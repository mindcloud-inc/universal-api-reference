# Export Knowledge Card to CSV with Tako

Exports a Tako knowledge card to CSV.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/csv`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [Export Knowledge Card to CSV](https://docs.tako.com/api-reference/export-csv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card_id` | query | `string` | yes | ID of the knowledge card to export as CSV. |
