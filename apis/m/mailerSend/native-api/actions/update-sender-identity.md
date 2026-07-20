# Update Sender Identity with MailerSend

## Endpoint

- **Method:** `PUT`
- **Path:** `/identities/:identity_id`
- **Base URL:** `https://api.mailersend.com/v1`
- **Official documentation:** [Update Sender Identity](https://developers.mailersend.com/api/v1/sender-identity#update-a-sender-identity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity_id` | path | `string` | yes | ID of the sender identity to update. |
| `name` | body | `string` | no | Updated display name for the sender identity. |
| `reply_to_email` | body | `string` | no | Updated reply-to email for the sender identity. |
| `reply_to_name` | body | `string` | no | Updated reply-to display name for the sender identity. |
