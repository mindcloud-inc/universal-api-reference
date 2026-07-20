# Get Parsed Data with Parsio

## Endpoint

- **Method:** `GET`
- **Path:** `/mailboxes/:mailbox_id/parsed`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Get Parsed Data](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `string` | yes | Parsio mailbox ID. |
| `page` | query | `number` | no | Page number. |
| `from` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date in YYYY-MM-DD format. |
