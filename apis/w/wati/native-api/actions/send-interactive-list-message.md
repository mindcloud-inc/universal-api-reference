# Send Interactive List Message with Wati

Sends an interactive list message in Wati.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sendInteractiveListMessage`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Send Interactive List Message](https://docs.wati.io/reference/post_api-v1-sendinteractivelistmessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsappNumber` | query | `string` | yes | Target recipient phone number. |
| `header` | body | `string` | no | Optional header text for the list message. |
| `body` | body | `string` | yes | Body text for the interactive list message. |
| `footer` | body | `string` | no | Optional footer text for the list message. |
| `buttonText` | body | `string` | yes | Text shown on the list picker button. |
| `sections[]` | body | `array<object>` | yes | Sections and rows for the list picker. |
