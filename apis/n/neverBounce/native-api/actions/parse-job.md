# Parse Job with NeverBounce

Updates an existing NeverBounce job by parsing its uploaded data.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/parse`
- **Base URL:** `https://api.neverbounce.com/v4.2`
- **Official documentation:** [Parse Job](https://developers.neverbounce.com/reference/jobs-parse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | body | `number` | yes | NeverBounce job identifier. |
| `auto_start` | body | `boolean` | no | Start the job automatically after parsing completes. |
