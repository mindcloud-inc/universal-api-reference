# CSV Import Delayed Job with FTrack

Creates a CSV import delayed job in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [CSV Import Delayed Job](https://developer.ftrack.com/api/operations/delayed-job-api-delayed-job-csvimportdelayedjob-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | CSV import job payload. |
