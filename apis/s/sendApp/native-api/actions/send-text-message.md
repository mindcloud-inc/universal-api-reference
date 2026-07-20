# Send Text Message with SendApp

## Endpoint

- **Method:** `GET`
- **Path:** `/send/text`
- **Base URL:** `https://official.sendapp.cloud/apiv3`
- **Official documentation:** [Send Text Message](https://official.sendapp.cloud/apiv3/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `footer` | query | `string` | no | Optional footer text. |
| `header` | query | `string` | no | Optional header text. |
| `message` | query | `string` | yes | Text message to send. |
| `number` | query | `string` | yes | WhatsApp number in international format with the + prefix. |
