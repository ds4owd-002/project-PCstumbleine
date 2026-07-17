# Processed Data

## Overview

This folder contains the analysis-ready dataset produced by cleaning and combining
the raw TDABC (Time-Driven Activity-Based Costing) observation files stored in
`data/raw/`. The data were generated through structured ridealong observation of
informal pit latrine emptiers ("gulpers") in Mzuzu, Malawi, as part of doctoral
research at ETH Zürich. Each row is one continuous interval during which a single
gulper performed a single subtask.

## Files

- `processed_data.csv` — the combined, cleaned dataset (all raw sessions row-bound
  together, with empty spacer columns and fully empty rows removed, and derived
  `job_date` and `source_file` columns added).
- `data dictionary.csv` — variable-level documentation (`variable_name`,
  `description`) for every column in `processed_data.csv`.
- `README.md` — this file.

## Source

Raw data: `data/raw/*.csv` (one file per observed job/session). **Raw files are
never modified** — all cleaning is performed in `docs/index.qmd` and written out
to this folder.

## Collection method

Data were recorded live in the field using a custom mobile data collection tool.
An enumerator timed one or more gulpers working in parallel on a single emptying
job, logging the start and end of each task interval as gulpers moved through the
job.

## Processing steps

1. Import each raw CSV from `data/raw/`.
2. Drop columns that are entirely `NA` (spacer columns from the collection tool)
   and rows that are entirely `NA`.
3. Add `job_date` (parsed from `job_id`) and `source_file` (raw filename) for
   provenance.
4. Row-bind all sessions into a single combined data frame.
5. Write the result to `processed_data.csv`.

## Privacy

Session-level metadata (exact date, location, enumerator identity) is held
privately outside this repository and is not included here. `gulper_id` is a
non-identifying numeric code and `job_id` only encodes the session date and
sequence number.

## License / reuse

Data are shared for the purposes of the Open Wash Data capstone course. Please
contact the author (Padraic Casserly, pcasserly@ethz.ch) before reuse outside
this course.
