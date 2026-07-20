# Create Campaign with MailoPost

Creates a new campaign in MailoPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/campaigns`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Create Campaign](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_email` | body | `string` | yes | Sender email address. |
| `subject` | body | `string` | yes | Campaign subject line. |
| `from_name` | body | `string` | no | Sender display name. |
| `text` | body | `string` | no | Plain-text campaign body. |
| `html` | body | `string` | yes | HTML campaign body. |
| `segment_id` | body | `string` | no | Segment ID to send the campaign to. |
| `lists[]` | body | `array<object>` | no | Recipient lists to send the campaign to. |
