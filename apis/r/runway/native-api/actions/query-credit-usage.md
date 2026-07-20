# Query Credit Usage with Runway

Retrieves organization credit usage from Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/organization/usage`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Query Credit Usage](https://docs.dev.runwayml.com/api#tag/Organization/paths/~1v1~1organization~1usage/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `beforeDate` | body | `string` | no | UTC exclusive end date in YYYY-MM-DD format. Defaults to tomorrow if omitted. |
| `startDate` | body | `string` | no | UTC start date in YYYY-MM-DD format for usage aggregation. Defaults to 30 days ago if omitted. |
