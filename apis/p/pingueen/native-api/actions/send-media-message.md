# Send Media Message with Pingueen

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.pingueen.it/ext/v2/{businessname}`
- **Official documentation:** [Send Media Message](https://etinet.gitbook.io/pingueen/api-reference/messages/freeform-messages/send-media-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client` | body | `string` | yes | Client ID to send the message to. |
| `client_name` | body | `string` | no | Client name used when sending by phone number. |
| `client_phone` | body | `string` | no | Client phone number with country prefix. |
| `delay` | body | `string` | no | Delay before sending, for example 10m or 2d. |
| `media` | body | `object` | yes | Media payload object with file URL and filename. |
| `message_type` | body | `string` | yes | Media message type, for example image or document. |
