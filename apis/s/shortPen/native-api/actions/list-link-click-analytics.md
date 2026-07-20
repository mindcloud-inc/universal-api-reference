# List Link Click Analytics with ShortPen

Retrieves click analytics for one ShortPen link by date range.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/analytics`
- **Base URL:** `https://api.shortpen.com`
- **Official documentation:** [List Link Click Analytics](https://shortpen.com/docs/api-reference/endpoint/analytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | body | `string` | yes | Inclusive start date in YYYY-MM-DD format. |
| `end` | body | `string` | yes | Inclusive end date in YYYY-MM-DD format. |
| `url_id` | body | `number` | yes | ShortPen link ID to filter analytics for a single link. |
| `workspace_id` | body | `number` | no | Optional workspace scope for the analytics export. |
