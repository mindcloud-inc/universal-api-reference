# Send a Whatsapp campaign with Routee

Sends a WhatsApp campaign with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send a Whatsapp campaign](https://docs.routee.net/reference/send-a-whatsapp-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The phone provided by the customer during the WABA account setup. It is the phone that receives the verification pin. |
| `to` | body | `string` | yes | The recipient of the message. Could be one of - phone number in international format. In this it should follow the guidelines of E.164 but leading 00 is as well accepted - group id |
| `text` | body | `string` | yes | The text to be sent. 4069 chars, UTF-8 support |
| `imageURL` | body | `string` | no | the url of the location where the image is stored. http or https, ASCII char set, supported formats are png, jpeg. Post-Processing Media Size 5MB. |
| `videoURL` | body | `string` | no | the url of the location where the video file is stored. http or https, ASCII char set, supported formats video/mp4, video/3gpp. Post-Processing media size 16MB. |
| `documentURL` | body | `string` | no | the url of the location where the document is stored. Any valid MIME-type is supported, post-Processing Media Size 100 MB. |
| `filename` | body | `string` | no | File name of the document to be shown. It is shown on the uploaded document when the channel supports this. Max 512 chars, UTF-8. |
| `caption` | body | `string` | no | Additional caption for the image / document / video. It is shown on the uploaded image / document / video when the Whatsapp supports this. Max 512 chars, UTF-8 |
| `audioURL` | body | `string` | no | the url of the location where the audio file is stored. Supported content is audio/aac, audio/mp4, audio/amr, audio/mpeg, audio/ogg; codecs=opus Note: The base audio/ogg type is not supported. Post-Processing Media Size 16MB |
| `stickerURL` | body | `string` | no | the url of the location where the sticker is stored. http or https, ASCII char set. Supported formats image/webp, post processing media size 100KB. |
| `longitude` | body | `number` | no | Longitude part of the coordinate. +/-180 |
| `latitude` | body | `number` | no | Latitude part of the coordinate. +/-180 |
| `locationName` | body | `string` | no | Optional name of location. 256 chars. |
| `locationAddress` | body | `string` | no | Optional address, will only be rendered if name is set. 256 chars. |
| `template` | body | `object` | no | The message template to be send. |
