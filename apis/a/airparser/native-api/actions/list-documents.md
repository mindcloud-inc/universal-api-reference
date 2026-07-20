# List Documents with Airparser

Retrieves documents from an Airparser inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/:inbox_id/docs`
- **Base URL:** `https://api.airparser.com`
- **Official documentation:** [List Documents](https://help.airparser.com/public-api/public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The Airparser inbox ID. |
| `page` | query | `number` | no | Page number for paginated document results. |
| `from` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date in YYYY-MM-DD format. |
| `q` | query | `string` | no | Text search query. |
| `statuses` | query | `list<string>` | no | Document statuses to include. |
