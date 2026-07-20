# Update Broadcast with Kit

Updates an existing broadcast in Kit.

## Endpoint

- **Method:** `PUT`
- **Path:** `/broadcasts/:id`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [Update Broadcast](https://developers.kit.com/api-reference/broadcasts/update-a-broadcast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Broadcast ID. |
| `subject` | body | `string` | yes | Email subject line. |
| `preview_text` | body | `string` | yes | Email preview text. |
| `content` | body | `string` | yes | HTML email content. |
| `description` | body | `string` | yes | Broadcast description. |
| `public` | body | `boolean` | yes | Publish broadcast to web when true. |
| `published_at` | body | `date` | yes | Published timestamp (ISO8601). |
| `send_at` | body | `date` | yes | Scheduled send timestamp (ISO8601). |
| `thumbnail_url` | body | `string` | yes | Thumbnail image URL. |
| `thumbnail_alt` | body | `string` | yes | Thumbnail alt text. |
| `email_template_id` | body | `number` | yes | ID of email template to use. |
| `email_address` | body | `string` | yes | Sending email address to use. |
| `subscriber_filter[]` | body | `array<object>` | yes | Subscriber targeting filter object array. |
