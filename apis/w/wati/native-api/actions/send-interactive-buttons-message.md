# Send Interactive Buttons Message with Wati

Sends an interactive button message in Wati.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sendInteractiveButtonsMessage`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Send Interactive Buttons Message](https://docs.wati.io/reference/post_api-v1-sendinteractivebuttonsmessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsappNumber` | query | `string` | yes | Target recipient phone number. |
| `header` | body | `object` | no | Optional interactive header payload. |
| `body` | body | `string` | yes | Body text for the interactive message. |
| `footer` | body | `string` | no | Optional footer text for the interactive message. |
| `buttons[]` | body | `array<object>` | yes | Interactive button definitions. |
