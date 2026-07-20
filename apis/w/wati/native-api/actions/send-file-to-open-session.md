# Send File to Open Session with Wati

Sends a file in an open Wati session.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sendSessionFile/:whatsappNumber`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Send File to Open Session](https://docs.wati.io/reference/post_api-v1-sendsessionfile-whatsappnumber)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsappNumber` | path | `string` | yes | WhatsApp phone number for the open session conversation. |
| `file` | body | `file` | yes | File to send in the active session. |
| `caption` | query | `string` | no | Optional caption for the file message. |
