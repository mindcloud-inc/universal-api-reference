# Request Feed Export with Dealfront

Creates a new feed export request in Dealfront.

## Endpoint

- **Method:** `POST`
- **Path:** `/export-requests`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [Request Feed Export](https://docs.leadfeeder.com/api/#request-a-feed-export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the account you want to export leads from. |
| `custom_feed_id` | body | `string` | yes | ID of the custom feed to export. Use all_leads to export all leads. |
| `start_date` | body | `string` | yes | Start date for the export window in YYYY-MM-DD format. |
| `end_date` | body | `string` | yes | End date for the export window in YYYY-MM-DD format. |
