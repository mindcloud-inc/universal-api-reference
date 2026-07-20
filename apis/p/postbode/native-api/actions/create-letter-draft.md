# Create Letter Draft with Postbode

Creates a draft letter in a Postbode mailbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/mailbox/:mailbox_id/letters`
- **Base URL:** `https://app.postbode.nu/api`
- **Official documentation:** [Create Letter Draft](https://github.com/postbode/postbode-api#send-letter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `number` | yes | The Postbode mailbox ID. |
| `documents[]` | body | `array<object>` | yes | One or more PDF documents to upload. |
| `name` | body | `string` | yes | The filename that Postbode should store for the PDF. |
| `content` | body | `string` | yes | The PDF file encoded as base64. |
| `envelope_id` | body | `number` | no | Envelope option ID for the outgoing letter. |
| `country` | body | `string` | no | Destination country code, for example NL. |
