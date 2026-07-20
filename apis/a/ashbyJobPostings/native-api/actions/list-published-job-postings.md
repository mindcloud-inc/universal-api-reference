# List Published Job Postings with Ashby Job Postings

Retrieves published job postings from a specific Ashby job board.

## Endpoint

- **Method:** `GET`
- **Path:** `/posting-api/job-board/:job_board_name`
- **Base URL:** `https://api.ashbyhq.com`
- **Official documentation:** [List Published Job Postings](https://developers.ashbyhq.com/docs/public-job-posting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_board_name` | path | `string` | yes | Required. The final path segment of the Ashby hosted jobs page URL, for example `Ashby` in `https://jobs.ashbyhq.com/Ashby`. |
| `includeCompensation` | query | `boolean` | no | Optional. When true, include compensation data for each returned job posting. |
