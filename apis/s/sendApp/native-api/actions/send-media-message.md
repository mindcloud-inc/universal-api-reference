# Send Media Message with SendApp

## Endpoint

- **Method:** `GET`
- **Path:** `/send/media`
- **Base URL:** `https://official.sendapp.cloud/apiv3`
- **Official documentation:** [Send Media Message](https://official.sendapp.cloud/apiv3/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | no | Optional filename sent with the media. |
| `media_url` | query | `string` | yes | Public URL of the file to send. |
| `message` | query | `string` | no | Optional caption for the media. |
| `number` | query | `string` | yes | WhatsApp number in international format with the + prefix. |
| `type` | query | `string` | yes | Media type to send: image, video, audio, or document. |
