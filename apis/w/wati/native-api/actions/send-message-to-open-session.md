# Send Message to Open Session with Wati

Sends a text message in an open Wati session.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sendSessionMessage/:whatsappNumber`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Send Message to Open Session](https://docs.wati.io/reference/post_api-v1-sendsessionmessage-whatsappnumber)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsappNumber` | path | `string` | yes | WhatsApp phone number for the open session conversation. |
| `messageText` | body | `string` | yes | Text to send in the active session. |
