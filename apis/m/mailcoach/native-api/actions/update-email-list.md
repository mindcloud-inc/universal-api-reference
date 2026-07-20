# Update Email List with Mailcoach

Updates an existing email list in Mailcoach.

## Endpoint

- **Method:** `PUT`
- **Path:** `/email-lists/:uuid`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [Update Email List](https://www.mailcoach.app/api-documentation/endpoints/email-lists/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allow_form_subscriptions` | body | `boolean` | no | Whether form subscriptions are allowed. |
| `campaigns_feed_enabled` | body | `boolean` | no | Whether the campaigns feed is enabled for the list. |
| `confirmation_mail` | body | `string` | no | The confirmation mail mode. |
| `confirmation_mail_content` | body | `string` | no | The content used for a custom confirmation email. |
| `confirmation_mail_subject` | body | `string` | no | The subject used for a custom confirmation email. |
| `default_from_email` | body | `string` | yes | The default sender email address. |
| `default_from_name` | body | `string` | no | The default sender name. |
| `default_reply_to_email` | body | `string` | no | The default reply-to email address. |
| `default_reply_to_name` | body | `string` | no | The default reply-to name. |
| `name` | body | `string` | yes | The name of the email list. |
| `redirect_after_already_subscribed` | body | `string` | no | URL to redirect to when the subscriber already exists. |
| `redirect_after_subscribed` | body | `string` | no | URL to redirect to after a successful subscription. |
| `redirect_after_subscription_pending` | body | `string` | no | URL to redirect to when confirmation is still pending. |
| `redirect_after_unsubscribed` | body | `string` | no | URL to redirect to after an unsubscribe. |
| `report_campaign_sent` | body | `boolean` | no | Whether to send campaign sent reports. |
| `report_campaign_summary` | body | `boolean` | no | Whether to send campaign summary reports. |
| `report_email_list_summary` | body | `boolean` | no | Whether to send email list summary reports. |
| `report_recipients` | body | `string` | no | Comma-delimited email addresses that should receive reports. |
| `requires_confirmation` | body | `boolean` | no | Whether subscribers must confirm before they are added. |
| `uuid` | path | `string` | yes | The UUID of the email list to update. |
