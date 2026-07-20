# Update Campaign with Emailchef

Updates an existing campaign in Emailchef.

## Endpoint

- **Method:** `PUT`
- **Path:** `campaigns/:id`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Update Campaign](https://emailchef.com/integration/#/Campaigns/updateCampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Emailchef campaign ID. |
| `instance_in.name` | body | `string` | no | Campaign name. |
| `instance_in.subject` | body | `string` | no | Email subject. |
| `instance_in.html_body` | body | `string` | no | HTML body. |
| `instance_in.text_body` | body | `string` | no | Text body. |
| `instance_in.sender_id` | body | `string` | no | Sender ID. |
| `instance_in.reply_to_id` | body | `string` | no | Reply-to sender ID. |
| `instance_in.confirmation_email_address` | body | `string` | no | Confirmation email address. |
| `instance_in.lists[]` | body | `array<object>` | no | Associated lists. |
| `instance_in.lists[].list_id` | body | `string` | no | List ID. |
| `instance_in.lists[].segment_id` | body | `string` | no | Segment ID. |
