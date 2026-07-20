# Send Single Chat with WhatsBoost

Sends a single chat message from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/send/whatsapp`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Send Single Chat](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | body | `string` | yes | WhatsApp account you want to use for sending. You can get the account unique ID from /get/wa.accounts or in the dashboard. |
| `recipient` | body | `string` | yes | Recipient mobile number or group address. Accepts WhatsApp group address or E.164 formatted number and locally formatted numbers using the country code from your profile settings. Example: E.164: +34612345678, Local: 612345678. |
| `type` | body | `string` | no | Type of WhatsApp message. |
| `message` | body | `string` | yes | Message or caption you want to send. Spintax is also supported. |
| `priority` | body | `number` | no | If you want to send the message as priority, it will be sent immediately. 1 for yes and 2 for no. |
| `media_file` | body | `string` | no | For 'media' type messages only. The media file you want to attach in the WhatsApp message. Supports jpg, png, gif, mp4, mp3, and ogg files. |
| `media_url` | body | `string` | no | For 'media' type messages only. The media file URL. Must be a direct link to the media file. Supports jpg, png, gif, mp4, mp3, and ogg files. |
| `media_type` | body | `string` | no | For 'media' type messages only. Required if using 'media_url'. Specifies the file type of the media in the provided URL. |
| `document_file` | body | `string` | no | For 'document' type messages only. The document file you want to attach in the WhatsApp message. Supports pdf, xml, xls, xlsx, doc, and docx files. |
| `document_url` | body | `string` | no | For 'document' type messages only. The document file URL. Must be a direct link to the document file. Supports pdf, xml, xls, xlsx, doc, and docx files. |
| `document_name` | body | `string` | no | For 'document' type with 'document_url' messages only. The document file name. Include the file extension (e.g., document.pdf). |
| `document_type` | body | `string` | no | For 'document' type messages only. Required if using 'document_url'. Specifies the file type of the document in the provided URL. |
| `shortener` | body | `number` | no | Shortener ID. Specify the shortener you want to use to shorten links in your message. Get the list of available shorteners from /get/shorteners. |
