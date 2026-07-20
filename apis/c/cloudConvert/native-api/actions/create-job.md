# Create Job with CloudConvert

Creates a job in your CloudConvert account.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Create Job](https://cloudconvert.com/docs/api-reference/jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tasks` | body | `object` | yes | Object containing one or more named CloudConvert tasks. |
| `tag` | body | `string` | no | Optional tag to identify the job. |
