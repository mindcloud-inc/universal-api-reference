# List Templates with Parsio

## Endpoint

- **Method:** `GET`
- **Path:** `/mailboxes/:mb_id/templates`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [List Templates](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mb_id` | path | `string` | yes | Parsio mailbox ID. |
| `page` | query | `number` | no | Page number. |
