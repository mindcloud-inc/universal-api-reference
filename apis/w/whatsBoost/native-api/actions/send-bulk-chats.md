# Send Bulk Chats with WhatsBoost

Sends bulk chat messages from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/send/whatsapp.bulk`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Send Bulk Chats](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | body | `string` | yes | WhatsApp account you want to use for sending. You can get the account unique ID from /get/wa.accounts or in the dashboard. |
| `campaign` | body | `string` | yes | Name of the campaign, you will see this in the WhatsApp campaign manager. |
| `recipients` | body | `string` | no | List of phone numbers or group addresses separated by commas. Optional if 'groups' parameter is not empty. Accepts WhatsApp group address, E.164 formatted number, or locally formatted numbers using the country code from your profile settings. |
| `groups` | body | `string` | no | List of contact group IDs separated by commas. Optional if 'recipients' parameter is not empty. You can get group IDs from /get/groups (Your contact groups). |
| `type` | body | `string` | yes | Type of WhatsApp message. |
| `message` | body | `string` | yes | Message or caption you want to send. Spintax and shortcodes are supported. |
| `media_file` | body | `string` | no | For 'media' type messages only. The media file to attach to the WhatsApp message. Supports jpg, png, gif, mp4, mp3, and ogg files. |
| `media_url` | body | `string` | no | For 'media' type messages only. URL to the media file. Must be a direct link. Supports jpg, png, gif, mp4, mp3, and ogg files. |
| `media_type` | body | `string` | no | For 'media' type messages only. Required if using 'media_url' instead of 'media_file'. Declares the file type of the media in the provided URL. |
| `document_file` | body | `string` | no | For 'document' type messages only. The document file to attach to the WhatsApp message. Supports pdf, xml, xls, xlsx, doc, and docx files. |
| `document_url` | body | `string` | no | For 'document' type messages only. URL to the document file. Must be a direct link. Supports pdf, xml, xls, xlsx, doc, and docx files. |
| `document_name` | body | `string` | no | For 'document' type messages with 'document_url'. File name of the document. Include the file extension (e.g., document.pdf). |
| `document_type` | body | `string` | no | For 'document' type messages only. Required if using 'document_url' instead of 'document_file'. Declares the file type of the document in the provided URL. |
| `shortener` | body | `number` | no | Shortener ID. Specify the shortener to use for shortening links in your message. Get the list of available shorteners from /get/shorteners. |
