# Create Broadcast with Kit

Creates a new broadcast in Kit.

## Endpoint

- **Method:** `POST`
- **Path:** `/broadcasts`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [Create Broadcast](https://developers.kit.com/api-reference/broadcasts/create-a-broadcast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | Email subject line. |
| `preview_text` | body | `string` | yes | Email preview text. |
| `content` | body | `string` | yes | HTML email content. |
| `description` | body | `string` | yes | Broadcast description. |
| `public` | body | `boolean` | yes | Publish broadcast to web when true. |
| `published_at` | body | `date` | yes | Published timestamp (ISO8601). |
| `subscriber_filter[]` | body | `array<object>` | yes | Subscriber targeting filter object array. |
| `email_template_id` | body | `number` | no | ID of email template to use. |
| `email_address` | body | `string` | no | Sending email address to use. |
| `send_at` | body | `date` | no | Scheduled send timestamp (ISO8601). |
| `thumbnail_url` | body | `string` | no | Thumbnail image URL. |
| `thumbnail_alt` | body | `string` | no | Thumbnail alt text. |
