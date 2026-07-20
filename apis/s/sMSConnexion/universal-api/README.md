# <img src="https://images.mindcloud.co/apps/icons/author-sms-connexion_1775243158143.png" alt="SMS Connexion logo" width="28" height="28"> SMS Connexion: Universal API

Send SMS, manage campaigns, and track messaging delivery across channels

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSConnexion/latest
- **Category:** Marketing
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sms.cx/
- **Vendor API docs:** https://sms.cx/sms-api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To Optouts](actions/add-contact-to-optouts.md) | POST | Adds contacts to the optout list in SMS Connexion. |
| [Cancel OTP](actions/cancel-otp.md) | DELETE | Deletes an existing OTP from SMS Connexion. |
| [Create OTP](actions/create-otp.md) | POST | Creates a new OTP in SMS Connexion. |
| [Estimate SMS](actions/estimate-sms.md) | GET | Estimates a new SMS in SMS Connexion. |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves the current account balance from SMS Connexion. |
| [Get Advanced Report](actions/get-advanced-report.md) | GET | Retrieves an advanced report from SMS Connexion. |
| [Get Bulk Number Lookup CSV Export](actions/get-bulk-number-lookup-csv-export.md) | GET | Retrieves a bulk lookup export from SMS Connexion as CSV. |
| [Get Bulk Number Lookup Status](actions/get-bulk-number-lookup-status.md) | GET | Retrieves a bulk number lookup result from SMS Connexion. |
| [Get Bulk Number Lookup XLSX Export](actions/get-bulk-number-lookup-xlsx-export.md) | GET | Retrieves a bulk lookup export from SMS Connexion as XLSX. |
| [Get Campaign Report](actions/get-campaign-report.md) | GET | Retrieves a campaign report from SMS Connexion. |
| [Get Campaign Report CSV Export](actions/get-campaign-report-csv-export.md) | GET | Retrieves a campaign report export from SMS Connexion as CSV. |
| [Get Campaign Report XLSX Export](actions/get-campaign-report-xlsx-export.md) | GET | Retrieves a campaign report export from SMS Connexion as XLSX. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from SMS Connexion. |
| [Get Conversation Read Status](actions/get-conversation-read-status.md) | GET |  |
| [Get Number Lookup Status](actions/get-number-lookup-status.md) | GET | Retrieves a number lookup result from SMS Connexion. |
| [Get OTP Status](actions/get-otp-status.md) | GET | Retrieves an OTP status from SMS Connexion. |
| [Get Report CSV Export](actions/get-report-csv-export.md) | GET | Retrieves an advanced report export from SMS Connexion as CSV. |
| [Get Report Message](actions/get-report-message.md) | GET | Retrieves a single message report from SMS Connexion. |
| [Get Report Summary](actions/get-report-summary.md) | GET | Retrieves summary reports by dimension from SMS Connexion. |
| [Get Report XLSX Export](actions/get-report-xlsx-export.md) | GET | Retrieves an advanced report export from SMS Connexion as XLSX. |
| [List Bulk Lookup Campaigns](actions/list-bulk-lookup-campaigns.md) | GET | Retrieves bulk lookup campaigns from SMS Connexion. |
| [List Campaign Reports](actions/list-campaign-reports.md) | GET | Retrieves sent campaigns from SMS Connexion. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from SMS Connexion. |
| [List Groups](actions/list-groups.md) | GET | Retrieves contact groups from SMS Connexion. |
| [List Optouts](actions/list-optouts.md) | GET | Retrieves opted-out contacts from SMS Connexion. |
| [List Originators](actions/list-originators.md) | GET | Retrieves available originators from SMS Connexion. |
| [List Templates](actions/list-templates.md) | GET | Retrieves message templates from SMS Connexion. |
| [Lookup Numbers In Bulk](actions/lookup-numbers-in-bulk.md) | POST | Creates a bulk number lookup in SMS Connexion. |
| [Lookup Single Number](actions/lookup-single-number.md) | GET | Looks up a phone number in SMS Connexion. |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS message with SMS Connexion. |
| [Send SMS In Conversation](actions/send-sms-in-conversation.md) | POST | Sends an SMS reply in SMS Connexion. |
| [Send Viber In Conversation](actions/send-viber-in-conversation.md) | POST | Sends a Viber reply in SMS Connexion. |
| [Send WhatsApp In Conversation](actions/send-whatsapp-in-conversation.md) | POST | Sends a WhatsApp reply in SMS Connexion. |
| [Validate Number](actions/validate-number.md) | GET | Validates a phone number in SMS Connexion. |
| [Verify OTP](actions/verify-otp.md) | PUT | Verifies an OTP in SMS Connexion. |

