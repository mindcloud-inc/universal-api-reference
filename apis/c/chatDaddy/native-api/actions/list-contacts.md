# List Contacts with ChatDaddy

Retrieves contact records from your ChatDaddy account.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [List Contacts](https://chatdaddy.stoplight.io/docs/openapi/6d5e4b6a5c72f-get-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Number of contacts to return. |
| `page` | query | `string` | no | Cursor for the next contact page. |
| `q` | query | `string` | no | Search contacts by text. |
