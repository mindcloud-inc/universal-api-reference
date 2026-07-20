# Get Candidate with 100Hires ATS

Retrieves a candidate from 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates/:id`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Get Candidate](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Candidate ID or alias to retrieve. |
| `include` | query | `string` | no | Optional include selector for related application summaries. |
