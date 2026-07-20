# List Documents with Parsio

## Endpoint

- **Method:** `GET`
- **Path:** `/mailboxes/:mailbox_id/docs`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [List Documents](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `string` | yes | Parsio mailbox ID. |
| `page` | query | `number` | no | Page number. |
| `from` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date in YYYY-MM-DD format. |
| `q` | query | `string` | no | Search query. |
| `status` | query | `list<string>` | no | Document status filter. |
