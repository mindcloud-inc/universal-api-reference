# Send Text Template with Pingueen

## Endpoint

- **Method:** `POST`
- **Path:** `/template`
- **Base URL:** `https://api.pingueen.it/ext/v2/{businessname}`
- **Official documentation:** [Send Text Template](https://etinet.gitbook.io/pingueen/api-reference/messages/templates/send-templates/send-text-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agents[]` | body | `array<string>` | no | List of agent emails assigned to the chat. |
| `callback_url` | body | `string` | no | Webhook URL for message status updates. |
| `client` | body | `string` | no | Client ID to send the template to. |
| `client_name` | body | `string` | no | Client name used when sending by phone number. |
| `client_phone` | body | `string` | no | Client phone number with country prefix. |
| `delay` | body | `string` | no | Delay before sending, for example 10m or 2d. |
| `template` | body | `object` | yes | Template object with name, language, and components. |
| `text_message` | body | `string` | no | Template text with placeholders such as {{1}}. |
