# List Candidate Activities with 100Hires ATS

Lists a candidate's activities in 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates/:id/activities`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [List Candidate Activities](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Candidate ID or alias to inspect activity history for. |
| `page` | query | `number` | no | Optional page number starting at 1. |
| `event_type` | query | `string` | no | Optional comma-separated activity event types to include. |
