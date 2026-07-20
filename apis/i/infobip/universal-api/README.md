# <img src="https://images.mindcloud.co/apps/icons/images-1_1774059473245.png" alt="Infobip logo" width="28" height="28"> Infobip: Universal API

Send and manage SMS, email, and 2FA messaging with Infobip.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/infobip/latest
- **Category:** Communication / Team Messaging
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.infobip.com/
- **Vendor API docs:** https://www.infobip.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Outbound SMS Delivery Reports](actions/get-outbound-sms-delivery-reports.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-outbound-sms-delivery-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### 2fa Application

| Action | Method | Description |
| --- | --- | --- |
| [Create 2FA Application](actions/create2fa-application.md) | POST |  |
| [Get 2FA Applications](actions/get2fa-applications.md) | GET |  |

### 2fa Pin

| Action | Method | Description |
| --- | --- | --- |
| [Send 2FA PIN Code Over SMS](actions/send2fa-pin-code-over-sms.md) | POST |  |
| [Verify 2FA PIN](actions/verify2fa-pin.md) | PUT |  |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET |  |

### Email Domain

| Action | Method | Description |
| --- | --- | --- |
| [Add Email Domain](actions/add-email-domain.md) | POST |  |
| [Delete Email Domain](actions/delete-email-domain.md) | DELETE |  |
| [Get Email Domain Details](actions/get-email-domain-details.md) | GET |  |
| [Get Email Domains](actions/get-email-domains.md) | GET |  |
| [Update Email Domain Tracking Events](actions/update-email-domain-tracking-events.md) | PUT |  |
| [Verify Email Domain](actions/verify-email-domain.md) | PUT |  |

### Email Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Message Logs](actions/get-email-message-logs.md) | GET |  |
| [Get Outbound Email Delivery Reports](actions/get-outbound-email-delivery-reports.md) | GET |  |
| [Send Email Messages](actions/send-email-messages.md) | POST |  |
| [Send Fully Featured Email](actions/send-fully-featured-email.md) | POST |  |

### Email Suppression

| Action | Method | Description |
| --- | --- | --- |
| [Add Email Suppressions](actions/add-email-suppressions.md) | POST |  |
| [Delete Email Suppressions](actions/delete-email-suppressions.md) | DELETE |  |
| [Get Email Suppressions](actions/get-email-suppressions.md) | GET |  |
| [Get Suppression Domains](actions/get-suppression-domains.md) | GET |  |

### Email Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Template](actions/create-email-template.md) | POST |  |
| [Delete Email Template](actions/delete-email-template.md) | DELETE |  |
| [Generate Email Template Preview](actions/generate-email-template-preview.md) | GET |  |
| [Get Email Template](actions/get-email-template.md) | GET |  |
| [Get Email Templates](actions/get-email-templates.md) | GET |  |
| [Update Email Template](actions/update-email-template.md) | PUT |  |

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Request Email Validations](actions/request-email-validations.md) | POST |  |
| [Validate Email Address](actions/validate-email-address.md) | POST |  |

### Inbound Sms

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbound SMS Messages](actions/get-inbound-sms-messages.md) | GET |  |

### Scheduled Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Scheduled Email Statuses](actions/get-scheduled-email-statuses.md) | GET |  |
| [Get Scheduled Emails](actions/get-scheduled-emails.md) | GET |  |
| [Reschedule Emails](actions/reschedule-emails.md) | PUT |  |
| [Update Scheduled Email Statuses](actions/update-scheduled-email-statuses.md) | PUT |  |

### Scheduled Sms

| Action | Method | Description |
| --- | --- | --- |
| [Get Scheduled SMS Message Status](actions/get-scheduled-sms-message-status.md) | GET |  |
| [Get Scheduled SMS Messages](actions/get-scheduled-sms-messages.md) | GET |  |
| [Reschedule SMS Messages](actions/reschedule-sms-messages.md) | PUT |  |
| [Update Scheduled SMS Message Status](actions/update-scheduled-sms-message-status.md) | PUT |  |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Outbound SMS Delivery Reports](actions/get-outbound-sms-delivery-reports.md) | GET |  |
| [Get Outbound SMS Message Logs](actions/get-outbound-sms-message-logs.md) | GET |  |
| [Preview SMS Message](actions/preview-sms-message.md) | GET |  |
| [Send SMS Message](actions/send-sms-message.md) | POST |  |

