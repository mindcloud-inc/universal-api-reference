# List Click Analytics with ShortPen

Retrieves click analytics from ShortPen for a date range.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/analytics`
- **Base URL:** `https://api.shortpen.com`
- **Official documentation:** [List Click Analytics](https://shortpen.com/docs/api-reference/endpoint/analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | body | `string` | yes | Inclusive start date in YYYY-MM-DD format. |
| `end` | body | `string` | yes | Inclusive end date in YYYY-MM-DD format. |
| `workspace_id` | body | `number` | no | Optional workspace scope for the analytics export. |
