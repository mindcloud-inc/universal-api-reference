# Infobip: Native API Reference

A consolidated summary of Infobip's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.infobip.com/docs/api
- **OpenAPI specification:** https://infobip-cdn-h0h7ekhqhgh4hgau.a02.azurefd.net/api-docs/production/openapi/infobip-openapi-specification.json.gz
- **API base URL:** `https://rkpzwe.api.infobip.com`

## Authentication

### API Key

Use an Infobip API key with the scopes required for the SMS, Email, Account, and 2FA endpoints you plan to use.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.infobip.com/docs/essentials/api-essentials/api-authorization)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Email Domain](actions/add-email-domain.md) | `POST /email/1/domains` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Add Email Suppressions](actions/add-email-suppressions.md) | `POST /email/1/suppressions` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Create Email Template](actions/create-email-template.md) | `POST /email/1/templates` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Create 2FA Application](actions/create2fa-application.md) | `POST /2fa/2/applications` | [docs](https://www.infobip.com/docs/api/platform/2fa/2fa-configuration/create-2fa-application) |
| [Delete Email Domain](actions/delete-email-domain.md) | `DELETE /email/1/domains/{domainName}` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Delete Email Suppressions](actions/delete-email-suppressions.md) | `DELETE /email/1/suppressions` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Delete Email Template](actions/delete-email-template.md) | `DELETE /email/1/templates/{templateId}` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Generate Email Template Preview](actions/generate-email-template-preview.md) | `POST /email/1/templates/{templateId}/preview` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /account/1/balance` | [docs](https://www.infobip.com/docs/essentials/api-essentials/api-authorization) |
| [Get Email Domain Details](actions/get-email-domain-details.md) | `GET /email/1/domains/{domainName}` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Email Domains](actions/get-email-domains.md) | `GET /email/1/domains` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Email Message Logs](actions/get-email-message-logs.md) | `GET /email/4/logs` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Email Suppressions](actions/get-email-suppressions.md) | `GET /email/1/suppressions` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Email Template](actions/get-email-template.md) | `GET /email/1/templates/{templateId}` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Email Templates](actions/get-email-templates.md) | `GET /email/1/templates` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Inbound SMS Messages](actions/get-inbound-sms-messages.md) | `GET /sms/1/inbox/reports` | [docs](https://www.infobip.com/docs/api/channels/sms/inbound-sms/get-inbound-sms-messages) |
| [Get Outbound Email Delivery Reports](actions/get-outbound-email-delivery-reports.md) | `GET /email/4/reports` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Outbound SMS Delivery Reports](actions/get-outbound-sms-delivery-reports.md) | `GET /sms/3/reports` | [docs](https://www.infobip.com/docs/api/channels/sms/logs-and-status-reports/get-outbound-sms-message-delivery-reports) |
| [Get Outbound SMS Message Logs](actions/get-outbound-sms-message-logs.md) | `GET /sms/3/logs` | [docs](https://www.infobip.com/docs/api/channels/sms) |
| [Get Scheduled Email Statuses](actions/get-scheduled-email-statuses.md) | `GET /email/1/bulks/status` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Scheduled Emails](actions/get-scheduled-emails.md) | `GET /email/1/bulks` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get Scheduled SMS Message Status](actions/get-scheduled-sms-message-status.md) | `GET /sms/1/bulks/status` | [docs](https://www.infobip.com/docs/api/channels/sms) |
| [Get Scheduled SMS Messages](actions/get-scheduled-sms-messages.md) | `GET /sms/1/bulks` | [docs](https://www.infobip.com/docs/api/channels/sms/outbound-sms/get-scheduled-sms-messages) |
| [Get Suppression Domains](actions/get-suppression-domains.md) | `GET /email/1/suppressions/domains` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Get 2FA Applications](actions/get2fa-applications.md) | `GET /2fa/2/applications` | [docs](https://www.infobip.com/docs/api/platform/2fa) |
| [Preview SMS Message](actions/preview-sms-message.md) | `POST /sms/1/preview` | [docs](https://www.infobip.com/docs/api/channels/sms/outbound-sms/preview-sms-message) |
| [Request Email Validations](actions/request-email-validations.md) | `POST /email/2/validations` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Reschedule Emails](actions/reschedule-emails.md) | `PUT /email/1/bulks` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Reschedule SMS Messages](actions/reschedule-sms-messages.md) | `PUT /sms/1/bulks` | [docs](https://www.infobip.com/docs/api/channels/sms/outbound-sms/reschedule-sms-messages) |
| [Send Email Messages](actions/send-email-messages.md) | `POST /email/4/messages` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Send Fully Featured Email](actions/send-fully-featured-email.md) | `POST /email/3/send` | [docs](https://www.infobip.com/docs/api/channels/email/send-fully-featured-email) |
| [Send SMS Message](actions/send-sms-message.md) | `POST /sms/3/messages` | [docs](https://www.infobip.com/docs/api/channels/sms/outbound-sms/send-sms-messages) |
| [Send 2FA PIN Code Over SMS](actions/send2fa-pin-code-over-sms.md) | `POST /2fa/2/pin` | [docs](https://www.infobip.com/docs/api/platform/2fa/pin-sending-and-verification/send-2fa-pin-code-over-sms) |
| [Update Email Domain Tracking Events](actions/update-email-domain-tracking-events.md) | `PUT /email/1/domains/{domainName}/tracking` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Update Email Template](actions/update-email-template.md) | `PUT /email/1/templates/{templateId}` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Update Scheduled Email Statuses](actions/update-scheduled-email-statuses.md) | `PUT /email/1/bulks/status` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Update Scheduled SMS Message Status](actions/update-scheduled-sms-message-status.md) | `PUT /sms/1/bulks/status` | [docs](https://www.infobip.com/docs/api/channels/sms/outbound-sms/update-scheduled-sms-messages-status) |
| [Validate Email Address](actions/validate-email-address.md) | `POST /email/2/validation` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Verify Email Domain](actions/verify-email-domain.md) | `POST /email/1/domains/{domainName}/verify` | [docs](https://www.infobip.com/docs/api/channels/email) |
| [Verify 2FA PIN](actions/verify2fa-pin.md) | `POST /2fa/2/pin/{pinId}/verify` | [docs](https://www.infobip.com/docs/api/platform/2fa/pin-sending-and-verification/verify-2fa-phone-number) |
