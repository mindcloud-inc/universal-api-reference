# <img src="https://images.mindcloud.co/apps/icons/sea-x_1776106378520.png" alt="SeaX logo" width="28" height="28"> SeaX: Universal API

SeaX by SeaSalt.ai provides workspace-scoped messaging, conversation, contact, campaign, phone, voice, and WhatsApp management APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/seaX/latest
- **Category:** Communication / Team Messaging
- **Actions:** 85
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://seax.seasalt.ai
- **Vendor API docs:** https://api.seasalt.ai/seax/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List API Keys](actions/list-api-keys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (85)

### Ai Agent

| Action | Method | Description |
| --- | --- | --- |
| [List AI Agents](actions/list-ai-agents.md) | GET | Retrieves AI agents from the current SeaX workspace. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates an API key in the current SeaX workspace. |
| [Delete API Key](actions/delete-api-key.md) | DELETE | Deletes an API key from the current SeaX workspace. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API keys from the current SeaX workspace. |
| [Reset API Keys](actions/reset-api-keys.md) | POST | Resets SeaX API keys and creates a replacement. |
| [Update API Key](actions/update-api-key.md) | PUT | Updates an API key in the current SeaX workspace. |

### Auto Dialer Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Auto Dialer Campaign](actions/create-auto-dialer-campaign.md) | POST | Creates an auto dialer campaign in SeaX. |
| [Delete Auto Dialer Campaign](actions/delete-auto-dialer-campaign.md) | DELETE | Deletes an auto dialer campaign from SeaX. |
| [Get Auto Dialer Campaign](actions/get-auto-dialer-campaign.md) | GET | Retrieves an auto dialer campaign from SeaX. |
| [List Auto Dialer Campaigns](actions/list-auto-dialer-campaigns.md) | GET | Retrieves auto dialer campaigns from SeaX. |
| [Update Auto Dialer Campaign](actions/update-auto-dialer-campaign.md) | PUT | Updates an auto dialer campaign in SeaX. |

### Auto Dialer Campaign Contact Template

| Action | Method | Description |
| --- | --- | --- |
| [Download Auto Dialer Campaign Contact Template](actions/download-auto-dialer-campaign-contact-template.md) | GET | Retrieves a contact template for a SeaX auto dialer campaign. |

### Auto Dialer Campaign Job

| Action | Method | Description |
| --- | --- | --- |
| [List Auto Dialer Campaign Jobs](actions/list-auto-dialer-campaign-jobs.md) | GET | Retrieves jobs for a SeaX auto dialer campaign. |

### Auto Dialer Campaign Log

| Action | Method | Description |
| --- | --- | --- |
| [List Auto Dialer Campaign Logs](actions/list-auto-dialer-campaign-logs.md) | GET | Retrieves logs for a SeaX auto dialer campaign. |

### Auto Dialer Campaign Logs

| Action | Method | Description |
| --- | --- | --- |
| [Download Auto Dialer Campaign Logs](actions/download-auto-dialer-campaign-logs.md) | GET | Retrieves a log download for a SeaX auto dialer campaign. |

### Auto Dialer Campaign Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Auto Dialer Campaign Results](actions/get-auto-dialer-campaign-results.md) | GET | Retrieves structured results for a SeaX auto dialer campaign. |

### Auto Dialer Campaign Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Auto Dialer Campaign Webhook](actions/create-auto-dialer-campaign-webhook.md) | POST | Creates a webhook for a SeaX auto dialer campaign. |

### Auto Dialer Contact Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Auto Dialer Campaign Contact File](actions/validate-auto-dialer-campaign-contact-file.md) | POST | Validates a contact file for a SeaX auto dialer campaign. |

### Auto Dialer Dry Run

| Action | Method | Description |
| --- | --- | --- |
| [Dry Run Auto Dialer Campaign](actions/dry-run-auto-dialer-campaign.md) | POST | Retrieves a dry run preview for a SeaX auto dialer campaign. |

### Auto Dialer Execution Callback

| Action | Method | Description |
| --- | --- | --- |
| [Callback Auto Dialer Campaign Execution](actions/callback-auto-dialer-campaign-execution.md) | POST |  |

### Auto Dialer Gather Callback

| Action | Method | Description |
| --- | --- | --- |
| [Callback Auto Dialer Campaign Gather](actions/callback-auto-dialer-campaign-gather.md) | POST |  |

### Auto Dialer Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Auto Dialer Campaign](actions/validate-auto-dialer-campaign.md) | POST | Validates a SeaX auto dialer campaign. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a campaign in the current SeaX workspace. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes a campaign from the current SeaX workspace. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from the current SeaX workspace. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from the current SeaX workspace. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates a campaign in the current SeaX workspace. |

### Campaign Contact Template

| Action | Method | Description |
| --- | --- | --- |
| [Download Campaign Contact Template](actions/download-campaign-contact-template.md) | GET | Retrieves a contact template for a SeaX campaign. |

### Campaign Contact Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Campaign Contact File](actions/validate-campaign-contact-file.md) | POST | Validates a contact file for a SeaX campaign. |

### Campaign Log

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Logs](actions/list-campaign-logs.md) | GET | Retrieves logs for a SeaX campaign. |

### Campaign Log Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Campaign Logs](actions/download-campaign-logs.md) | GET | Retrieves a log download for a SeaX campaign. |

### Campaign Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign Webhook](actions/create-campaign-webhook.md) | POST | Creates a webhook for a SeaX campaign. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in the current SeaX workspace. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from the current SeaX workspace. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from the current SeaX workspace. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in the current SeaX workspace. |

### Contact Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Contacts](actions/import-contacts.md) | POST | Imports contacts into SeaX from a CSV file. |

### Contact Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Label](actions/create-contact-label.md) | POST | Creates a contact label in the current SeaX workspace. |
| [Delete Contact Label](actions/delete-contact-label.md) | DELETE | Deletes a contact label from the current SeaX workspace. |
| [List Contact Labels](actions/list-contact-labels.md) | GET | Retrieves contact labels from the current SeaX workspace. |
| [Update Contact Label](actions/update-contact-label.md) | PUT | Updates a contact label in the current SeaX workspace. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from the current SeaX workspace. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from the current SeaX workspace. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates a conversation in the current SeaX workspace. |

### General Call Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create General Call Campaign](actions/create-general-call-campaign.md) | POST | Creates a general call campaign in SeaX. |

### General Sms Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create General SMS Campaign](actions/create-general-sms-campaign.md) | POST | Creates a general SMS campaign in SeaX. |

### General Wabp Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create General WABP Campaign](actions/create-general-wabp-campaign.md) | POST | Creates a general WhatsApp campaign in SeaX. |

### Highly Structured Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Highly Structured Message](actions/send-highly-structured-message.md) | POST | Sends a structured WhatsApp message from SeaX. |

### Highly Structured Message Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Highly Structured Message Campaign](actions/create-highly-structured-message-campaign.md) | POST | Creates a WhatsApp template campaign in SeaX. |

### Instagram Integration

| Action | Method | Description |
| --- | --- | --- |
| [Delete Instagram Integration](actions/delete-instagram-integration.md) | DELETE | Deletes an Instagram integration from SeaX by phone. |
| [Get Instagram Integration](actions/get-instagram-integration.md) | GET | Retrieves Instagram integration settings from SeaX by phone. |
| [Upsert Instagram Integration](actions/upsert-instagram-integration.md) | PUT | Updates Instagram integration settings in SeaX. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from the current SeaX workspace. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from the current SeaX workspace. |

### Line Official Integration

| Action | Method | Description |
| --- | --- | --- |
| [Delete LINE Official Integration](actions/delete-line-official-integration.md) | DELETE | Deletes a LINE Official integration from SeaX by phone. |
| [Get LINE Official Integration](actions/get-line-official-integration.md) | GET | Retrieves LINE Official integration settings from SeaX by phone. |
| [Upsert LINE Official Integration](actions/upsert-line-official-integration.md) | PUT | Updates LINE Official integration settings in SeaX. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET | Retrieves messages for a SeaX conversation. |
| [List Messages](actions/list-messages.md) | GET | Finds messages in SeaX by filter criteria. |
| [Send Message](actions/send-message.md) | POST | Sends an SMS or MMS message from SeaX. |
| [Send WABP Template Message](actions/send-wabp-template-message.md) | POST | Sends a WhatsApp template message from SeaX. |

### Messaging Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Messaging Service](actions/get-messaging-service.md) | GET | Retrieves a messaging service from SeaX. |
| [List Messaging Services](actions/list-messaging-services.md) | GET | Retrieves messaging services from the current SeaX workspace. |

### Messenger Integration

| Action | Method | Description |
| --- | --- | --- |
| [Delete Messenger Integration](actions/delete-messenger-integration.md) | DELETE | Deletes a Messenger integration from SeaX by phone. |
| [Get Messenger Integration](actions/get-messenger-integration.md) | GET | Retrieves Messenger integration settings from SeaX by phone. |
| [Upsert Messenger Integration](actions/upsert-messenger-integration.md) | PUT | Updates Messenger integration settings in SeaX. |

### Phone

| Action | Method | Description |
| --- | --- | --- |
| [Create Phone](actions/create-phone.md) | POST | Creates a phone number in the current SeaX workspace. |
| [Delete Phone](actions/delete-phone.md) | DELETE | Deletes a phone number from the current SeaX workspace. |
| [List Phones](actions/list-phones.md) | GET | Retrieves phone numbers from the current SeaX workspace. |
| [Update Phone](actions/update-phone.md) | PUT | Updates a phone number in the current SeaX workspace. |

### Phone Query

| Action | Method | Description |
| --- | --- | --- |
| [Query Phone](actions/query-phone.md) | POST |  |

### Phone Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Unset Phone Recipient](actions/unset-phone-recipient.md) | PUT | Updates a SeaX phone by clearing its recipient. |

### Phone Revision

| Action | Method | Description |
| --- | --- | --- |
| [List Phone Revisions](actions/list-phone-revisions.md) | GET | Retrieves revisions for a SeaX phone number. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS Message](actions/send-sms-message.md) | POST | Sends a direct SMS message from SeaX. |

### User Activity Log

| Action | Method | Description |
| --- | --- | --- |
| [List User Activity Logs](actions/list-user-activity-logs.md) | GET | Retrieves user activity logs from the current SeaX workspace. |

### Verified Caller

| Action | Method | Description |
| --- | --- | --- |
| [Unset Verified Caller](actions/unset-verified-caller.md) | PUT | Updates a SeaX phone by unsetting its verified caller. |

### Voice Call Session

| Action | Method | Description |
| --- | --- | --- |
| [List Voice Call Sessions](actions/list-voice-call-sessions.md) | GET | Retrieves voice call sessions from SeaX. |
| [Refresh Voice Call Session](actions/refresh-voice-call-session.md) | PUT | Updates voice call session statistics in SeaX. |

### Whatsapp Business Platform Account

| Action | Method | Description |
| --- | --- | --- |
| [Delete WhatsApp Business Platform Account](actions/delete-whatsapp-business-platform-account.md) | DELETE | Deletes a WhatsApp Business Platform account from SeaX. |
| [List WhatsApp Business Platform Accounts](actions/list-whatsapp-business-platform-accounts.md) | GET | Retrieves WhatsApp Business Platform accounts from SeaX. |
| [Resync WhatsApp Business Platform Account](actions/resync-whatsapp-business-platform-account.md) | PUT | Updates a SeaX WhatsApp Business Platform account by resyncing it. |
| [Sync WhatsApp Business Platform By Code](actions/sync-whatsapp-business-platform-by-code.md) | POST | Adds a WhatsApp Business Platform account to SeaX by code. |

### Whatsapp Message

| Action | Method | Description |
| --- | --- | --- |
| [Send WABP Message](actions/send-wabp-message.md) | POST | Sends a direct WhatsApp message from SeaX. |

### Whatsapp Template

| Action | Method | Description |
| --- | --- | --- |
| [List WhatsApp Business Platform Highly Structured Templates](actions/list-whatsapp-business-platform-highly-structured-templates.md) | GET | Retrieves WhatsApp template options from SeaX by phone number. |
| [List WhatsApp Business Platform Templates](actions/list-whatsapp-business-platform-templates.md) | GET | Retrieves WhatsApp Business Platform templates from SeaX. |

