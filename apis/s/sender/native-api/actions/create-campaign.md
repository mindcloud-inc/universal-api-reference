# Create Campaign with Sender

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Create Campaign](https://api.sender.net/campaigns/create-campaign/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Name of the campaign shown in reports. |
| `subject` | body | `string` | yes | Choose the subject of the campaign. |
| `from` | body | `string` | yes | Sender name to be shown to subscribers. |
| `reply_to` | body | `string` | yes | Verified reply-to email address. |
| `content_type` | body | `string` | yes | One of editor, html, or text. |
| `preheader` | body | `string` | no | Email preview text. |
| `groups[]` | body | `array<string>` | no | Group IDs that the campaign will be sent to. |
| `segments[]` | body | `array<string>` | no | Segment IDs that the campaign will be sent to. |
| `content` | body | `string` | no | Campaign content for html or text campaigns. |
