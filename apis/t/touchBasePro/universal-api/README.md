# <img src="https://images.mindcloud.co/apps/icons/touch-base-pro_1774635799857.png" alt="TouchBasePro logo" width="28" height="28"> TouchBasePro: Universal API

Manage email campaigns, SMS messaging, and email validation

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/touchBasePro/latest
- **Category:** Marketing
- **Actions:** 124
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.touchbasepro.com/
- **Vendor API docs:** https://developer.touchbasepro.com/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Validation Credit Balance](actions/get-validation-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-validation-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (124)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from TouchBasePro. |

### Campaign Bounce

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Bounces](actions/list-campaign-bounces.md) | GET | Retrieves campaign bounce details from TouchBasePro. |

### Campaign Click

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Clicks](actions/list-campaign-clicks.md) | GET | Retrieves campaign click details from TouchBasePro. |

### Campaign Draft

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign From Template](actions/create-campaign-from-template.md) | POST | Creates a new campaign from a template in TouchBasePro. |
| [Create Draft Campaign](actions/create-draft-campaign.md) | POST | Creates a new draft campaign in TouchBasePro. |

### Campaign Email Client Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Email Client Usage](actions/get-campaign-email-client-usage.md) | GET | Retrieves campaign email client usage from TouchBasePro. |

### Campaign Lists And Segments

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Lists And Segments](actions/get-campaign-lists-and-segments.md) | GET | Retrieves campaign lists and segments from TouchBasePro. |

### Campaign Open

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Opens](actions/list-campaign-opens.md) | GET | Retrieves campaign open details from TouchBasePro. |

### Campaign Preview

| Action | Method | Description |
| --- | --- | --- |
| [Send Campaign Preview](actions/send-campaign-preview.md) | POST | Sends a campaign preview in TouchBasePro. |

### Campaign Recipient

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Recipients](actions/list-campaign-recipients.md) | GET | Retrieves campaign recipients from TouchBasePro. |

### Campaign Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Unschedule Campaign](actions/unschedule-campaign.md) | PUT | Unschedules an existing campaign in TouchBasePro. |

### Campaign Send

| Action | Method | Description |
| --- | --- | --- |
| [Send Draft Campaign](actions/send-draft-campaign.md) | POST | Sends a draft campaign in TouchBasePro. |

### Campaign Spam Complaint

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Spam Complaints](actions/list-campaign-spam-complaints.md) | GET | Retrieves campaign spam complaints from TouchBasePro. |

### Campaign Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Summary](actions/get-campaign-summary.md) | GET | Retrieves a campaign summary from TouchBasePro. |

### Campaign Unsubscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Unsubscribers](actions/list-campaign-unsubscribers.md) | GET | Retrieves campaign unsubscribers from TouchBasePro. |

### Classic Email Send

| Action | Method | Description |
| --- | --- | --- |
| [Send Classic Email](actions/send-classic-email.md) | POST | Sends a classic email in TouchBasePro. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves supported country options from TouchBasePro. |

### Draft Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Draft Campaigns](actions/list-draft-campaigns.md) | GET | Retrieves draft campaigns from TouchBasePro. |

### Email Client

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Client](actions/get-email-client.md) | GET | Retrieves an email client from TouchBasePro. |

### Email Client Segment

| Action | Method | Description |
| --- | --- | --- |
| [List Email Client Segments](actions/list-email-client-segments.md) | GET | Retrieves email client segments from TouchBasePro. |

### Email Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Credit Balance](actions/get-email-credit-balance.md) | GET | Retrieves email credit balance from TouchBasePro. |

### Email Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in TouchBasePro. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from TouchBasePro. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from TouchBasePro. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates an existing custom field in TouchBasePro. |
| [Update Custom Field Options](actions/update-custom-field-options.md) | PUT | Updates existing custom field options in TouchBasePro. |

### Email List

| Action | Method | Description |
| --- | --- | --- |
| [Create Email List](actions/create-email-list.md) | POST | Creates a new email list in TouchBasePro. |
| [Delete Email List](actions/delete-email-list.md) | DELETE | Deletes an existing email list from TouchBasePro. |
| [Get Email List](actions/get-email-list.md) | GET | Retrieves an email list from TouchBasePro. |
| [List Email Lists](actions/list-email-lists.md) | GET | Retrieves available email lists from TouchBasePro. |
| [Update Email List](actions/update-email-list.md) | PUT | Updates an existing email list in TouchBasePro. |

### Email List Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Get Lists For Email](actions/get-lists-for-email.md) | GET | Retrieves lists for an email address from TouchBasePro. |

### Email List Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get List Stats](actions/get-list-stats.md) | GET | Retrieves statistics for a list from TouchBasePro. |

### Email List Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Active Subscribers in List](actions/list-active-subscribers-in-list.md) | GET | Retrieves active subscribers in a list from TouchBasePro. |
| [List Bounced Subscribers in List](actions/list-bounced-subscribers-in-list.md) | GET | Retrieves bounced subscribers in a list from TouchBasePro. |
| [List Deleted Subscribers in List](actions/list-deleted-subscribers-in-list.md) | GET | Retrieves deleted subscribers in a list from TouchBasePro. |
| [List Unconfirmed Subscribers in List](actions/list-unconfirmed-subscribers-in-list.md) | GET | Retrieves unconfirmed subscribers in a list from TouchBasePro. |
| [List Unsubscribed Subscribers in List](actions/list-unsubscribed-subscribers-in-list.md) | GET | Retrieves unsubscribed subscribers in a list from TouchBasePro. |

### Email Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in TouchBasePro. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from TouchBasePro. |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from TouchBasePro. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from TouchBasePro. |
| [Update Segment](actions/update-segment.md) | PUT | Updates an existing segment in TouchBasePro. |

### Email Segment Rule Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Rule Group To Segment](actions/add-rule-group-to-segment.md) | POST | Adds a rule group to a segment in TouchBasePro. |
| [Delete Segment Rules](actions/delete-segment-rules.md) | DELETE | Deletes existing segment rules from TouchBasePro. |

### Email Segment Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Active Subscribers in Segment](actions/list-active-subscribers-in-segment.md) | GET | Retrieves active subscribers in a segment from TouchBasePro. |

### Email Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Statistics](actions/get-email-statistics.md) | GET | Retrieves email statistics details from TouchBasePro. |

### Email Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Subscriber](actions/create-email-subscriber.md) | POST | Creates a new email subscriber in TouchBasePro. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from TouchBasePro. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves subscriber details from your TouchBasePro account. |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | PUT | Unsubscribes a subscriber in TouchBasePro. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in TouchBasePro. |

### Email Subscriber History

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriber History](actions/get-subscriber-history.md) | GET | Retrieves subscriber history details from TouchBasePro. |

### Email Subscriber Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Subscribers](actions/import-subscribers.md) | POST | Imports subscribers into your TouchBasePro account. |

### Email Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Template](actions/create-email-template.md) | POST | Creates a new email template in TouchBasePro. |
| [Delete Email Template](actions/delete-email-template.md) | DELETE | Deletes an existing email template from TouchBasePro. |
| [Get Email Template](actions/get-email-template.md) | GET | Retrieves an email template from TouchBasePro. |
| [Update Email Template](actions/update-email-template.md) | PUT | Updates an existing email template in TouchBasePro. |

### Email Template List

| Action | Method | Description |
| --- | --- | --- |
| [List Client Templates](actions/list-client-templates.md) | GET | Retrieves client email templates from TouchBasePro. |

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email Address](actions/validate-email-address.md) | GET | Validates an email address in TouchBasePro. |

### Email Validation Job

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email List](actions/validate-email-list.md) | POST | Validates an email list in TouchBasePro. |

### Email Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Activate Webhook](actions/activate-webhook.md) | PUT | Activates an existing webhook in TouchBasePro. |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in TouchBasePro. |
| [Deactivate Webhook](actions/deactivate-webhook.md) | PUT | Deactivates an existing webhook in TouchBasePro. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from TouchBasePro. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves configured webhooks from TouchBasePro. |
| [Test Webhook](actions/test-webhook.md) | GET | Tests an existing webhook in TouchBasePro. |

### Scheduled Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Scheduled Campaigns](actions/list-scheduled-campaigns.md) | GET | Retrieves scheduled campaigns from TouchBasePro. |

### Sent Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | GET | Retrieves sent campaigns from TouchBasePro. |

### Smart Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Smart Email Details](actions/get-smart-email-details.md) | GET | Retrieves smart email details from TouchBasePro. |
| [Get Smart Email List](actions/get-smart-email-list.md) | GET | Retrieves a smart email list from TouchBasePro. |

### Smart Email Group

| Action | Method | Description |
| --- | --- | --- |
| [List Smart Email Groups](actions/list-smart-email-groups.md) | GET | Retrieves smart email groups from TouchBasePro. |

### Smart Email Send

| Action | Method | Description |
| --- | --- | --- |
| [Send Smart Email](actions/send-smart-email.md) | POST | Sends a smart email in TouchBasePro. |

### Sms Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Campaign](actions/get-sms-campaign.md) | GET | Retrieves an SMS campaign from TouchBasePro. |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | GET | Retrieves SMS campaigns from your TouchBasePro account. |

### Sms Campaign Report

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Campaign Report](actions/get-sms-campaign-report.md) | GET | Retrieves an SMS campaign report from TouchBasePro. |

### Sms Campaign Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS Campaign Webhook](actions/create-sms-campaign-webhook.md) | POST | Creates a new SMS campaign webhook in TouchBasePro. |
| [Delete SMS Campaign Webhook](actions/delete-sms-campaign-webhook.md) | DELETE | Deletes an existing SMS campaign webhook from TouchBasePro. |
| [Get SMS Campaign Webhook](actions/get-sms-campaign-webhook.md) | GET | Retrieves an SMS campaign webhook from TouchBasePro. |
| [List SMS Campaign Webhooks](actions/list-sms-campaign-webhooks.md) | GET | Retrieves SMS campaign webhooks from TouchBasePro. |
| [Update SMS Campaign Webhook](actions/update-sms-campaign-webhook.md) | PUT | Updates an existing SMS campaign webhook in TouchBasePro. |

### Sms Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Credit Balance](actions/get-sms-credit-balance.md) | GET | Retrieves SMS credit balance from TouchBasePro. |

### Sms List

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS List](actions/create-sms-list.md) | POST | Creates a new SMS list in TouchBasePro. |
| [Delete SMS List](actions/delete-sms-list.md) | DELETE | Deletes an existing SMS list from TouchBasePro. |
| [Get SMS List](actions/get-sms-list.md) | GET | Retrieves an SMS list from TouchBasePro. |
| [List SMS Lists](actions/list-sms-lists.md) | GET | Retrieves SMS lists from TouchBasePro. |
| [Update SMS List](actions/update-sms-list.md) | PUT | Updates an existing SMS list in TouchBasePro. |

### Sms List Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS List Webhook](actions/create-sms-list-webhook.md) | POST | Creates a new SMS list webhook in TouchBasePro. |
| [Delete SMS List Webhook](actions/delete-sms-list-webhook.md) | DELETE | Deletes an existing SMS list webhook from TouchBasePro. |
| [Get SMS List Webhook](actions/get-sms-list-webhook.md) | GET | Retrieves an SMS list webhook from TouchBasePro. |
| [List SMS List Webhooks](actions/list-sms-list-webhooks.md) | GET | Retrieves SMS list webhooks from TouchBasePro. |
| [Update SMS List Webhook](actions/update-sms-list-webhook.md) | PUT | Updates an existing SMS list webhook in TouchBasePro. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Message](actions/get-sms-message.md) | GET | Retrieves an SMS message from TouchBasePro. |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS in TouchBasePro. |

### Sms Message Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS Message Webhook](actions/create-sms-message-webhook.md) | POST | Creates a new SMS message webhook in TouchBasePro. |
| [Delete SMS Message Webhook](actions/delete-sms-message-webhook.md) | DELETE | Deletes an existing SMS message webhook from TouchBasePro. |
| [Get SMS Message Status Webhook](actions/get-sms-message-status-webhook.md) | GET | Retrieves an SMS message status webhook from TouchBasePro. |
| [List SMS Message Webhooks](actions/list-sms-message-webhooks.md) | GET | Retrieves SMS message webhooks from TouchBasePro. |
| [Update SMS Message Webhook](actions/update-sms-message-webhook.md) | PUT | Updates an existing SMS message webhook in TouchBasePro. |

### Sms Reply Forward

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Reply Forward](actions/get-sms-reply-forward.md) | GET | Retrieves SMS reply forwarding from TouchBasePro. |
| [Set SMS Reply Forward](actions/set-sms-reply-forward.md) | POST | Sets SMS reply forwarding in TouchBasePro. |

### Sms Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS Subscriber](actions/create-sms-subscriber.md) | POST | Creates a new SMS subscriber in TouchBasePro. |
| [Delete SMS Subscriber](actions/delete-sms-subscriber.md) | DELETE | Deletes an existing SMS subscriber from TouchBasePro. |
| [Get SMS Subscriber](actions/get-sms-subscriber.md) | GET | Retrieves an SMS subscriber from TouchBasePro. |
| [List SMS Subscribers](actions/list-sms-subscribers.md) | GET | Retrieves SMS subscribers from TouchBasePro. |
| [Update SMS Subscriber](actions/update-sms-subscriber.md) | PUT | Updates an existing SMS subscriber in TouchBasePro. |

### Sms Subscriber Import

| Action | Method | Description |
| --- | --- | --- |
| [Import SMS Subscribers](actions/import-sms-subscribers.md) | POST | Imports SMS subscribers into TouchBasePro. |

### Suppressed Email Address

| Action | Method | Description |
| --- | --- | --- |
| [Suppress Email Addresses](actions/suppress-email-addresses.md) | POST | Suppresses existing email addresses in TouchBasePro. |
| [Unsuppress Email Address](actions/unsuppress-email-address.md) | PUT | Unsuppresses an email address in TouchBasePro. |

### Suppression List

| Action | Method | Description |
| --- | --- | --- |
| [Get Suppression List](actions/get-suppression-list.md) | GET | Retrieves the suppression list from TouchBasePro. |

### System Time

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Time](actions/get-current-time.md) | GET | Retrieves current time from TouchBasePro. |

### Time Zone

| Action | Method | Description |
| --- | --- | --- |
| [List Time Zones](actions/list-time-zones.md) | GET | Retrieves available time zones from TouchBasePro. |

### Transactional Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from TouchBasePro. |
| [Resend Email Message](actions/resend-email-message.md) | POST | Resends an email message in TouchBasePro. |

### Transactional Message Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Timeline](actions/get-message-timeline.md) | GET | Retrieves message timeline details from TouchBasePro. |

### Validation Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation Credit Balance](actions/get-validation-credit-balance.md) | GET | Retrieves validation credit balance from TouchBasePro. |

### Validation Job Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation List Status](actions/get-validation-list-status.md) | GET | Retrieves validation list status from TouchBasePro. |

### Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Download Validation Result](actions/download-validation-result.md) | GET | Downloads a validation result from TouchBasePro. |

### Whatsapp Event

| Action | Method | Description |
| --- | --- | --- |
| [WhatsApp Track Events](actions/whatsapp-track-events.md) | POST | Tracks WhatsApp events in your TouchBasePro account. |

### Whatsapp Media Upload

| Action | Method | Description |
| --- | --- | --- |
| [WhatsApp Upload Media](actions/whatsapp-upload-media.md) | POST | Uploads WhatsApp media files to TouchBasePro. |

### Whatsapp Message

| Action | Method | Description |
| --- | --- | --- |
| [WhatsApp Send Text Message](actions/whatsapp-send-text-message.md) | POST | Sends a WhatsApp text message in TouchBasePro. |

### Whatsapp Template

| Action | Method | Description |
| --- | --- | --- |
| [WhatsApp Create Template](actions/whatsapp-create-template.md) | POST | Creates a new WhatsApp template in TouchBasePro. |

### Whatsapp User

| Action | Method | Description |
| --- | --- | --- |
| [WhatsApp Get Users](actions/whatsapp-get-users.md) | GET | Retrieves WhatsApp user records from TouchBasePro. |

### Whatsapp User Event

| Action | Method | Description |
| --- | --- | --- |
| [WhatsApp Track User](actions/whatsapp-track-user.md) | POST | Tracks a WhatsApp user in TouchBasePro. |

