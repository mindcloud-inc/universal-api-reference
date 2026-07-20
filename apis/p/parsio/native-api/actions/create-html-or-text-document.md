# Create HTML or Text Document with Parsio

## Endpoint

- **Method:** `POST`
- **Path:** `/mailboxes/:mailbox_id/doc`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Create HTML or Text Document](https://help.parsio.io/public-api/parse-html-and-text-documents-using-api-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `string` | yes | Parsio mailbox ID. |
| `name` | body | `string` | yes | Document name or email subject. |
| `html` | body | `string` | no | HTML content to parse. |
| `text` | body | `string` | no | Plain text content to parse. |
| `from` | body | `string` | no | From email address. |
| `to` | body | `string` | no | To email address. |
| `meta` | body | `object` | no | Optional metadata object included as __meta__ in parsed output. |
