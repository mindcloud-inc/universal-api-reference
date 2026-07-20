# SMS Connexion: Native API Reference

A consolidated summary of SMS Connexion's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://sms.cx/sms-api-documentation/
- **API base URL:** `https://api.sms.cx`

## Authentication

### OAuth2

OAuth2 client credentials for SMS Connexion API

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.sms.cx/oauth/token to approve access.
2. Exchange the returned authorization code with a POST request to https://api.sms.cx/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `sms conversations reports groups originators templates shortlinks attachments optouts account applications firewall numbers lookup otp`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://sms.cx/sms-api-documentation/)

## API conventions

The next-page cursor is read from `paging.next`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–500). Use `next` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact To Optouts](actions/add-contact-to-optouts.md) | `POST /optouts` | [docs](https://sms.cx/sms-api-documentation/#operation/AddContactToOptoutsList) |
| [Cancel OTP](actions/cancel-otp.md) | `DELETE /otp/:otpId` | [docs](https://sms.cx/sms-api-documentation/#operation/CancelOtp) |
| [Create OTP](actions/create-otp.md) | `POST /otp` | [docs](https://sms.cx/sms-api-documentation/#operation/NewOtp) |
| [Estimate SMS](actions/estimate-sms.md) | `POST /sms/estimate` | [docs](https://sms.cx/sms-api-documentation/#operation/EstimateSms) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /account/balance` | [docs](https://sms.cx/sms-api-documentation/#operation/GetAccountBalance) |
| [Get Advanced Report](actions/get-advanced-report.md) | `GET /reports` | [docs](https://sms.cx/sms-api-documentation/#operation/GetAdvancedReport) |
| [Get Bulk Number Lookup CSV Export](actions/get-bulk-number-lookup-csv-export.md) | `GET /numbers/lookup/lookupBulkId/:lookupBulkId/csv` | [docs](https://sms.cx/sms-api-documentation/#operation/ExportNumberLookupReportToCSV) |
| [Get Bulk Number Lookup Status](actions/get-bulk-number-lookup-status.md) | `GET /numbers/lookup/lookupBulkId/:lookupBulkId` | [docs](https://sms.cx/sms-api-documentation/#operation/GetBulkLookupStatus) |
| [Get Bulk Number Lookup XLSX Export](actions/get-bulk-number-lookup-xlsx-export.md) | `GET /numbers/lookup/lookupBulkId/:lookupBulkId/xlsx` | [docs](https://sms.cx/sms-api-documentation/#operation/ExportNumberLookupReportToXLSX) |
| [Get Campaign Report](actions/get-campaign-report.md) | `GET /reports/campaigns/:campaignId` | [docs](https://sms.cx/sms-api-documentation/#operation/GetCampaignReport) |
| [Get Campaign Report CSV Export](actions/get-campaign-report-csv-export.md) | `GET /reports/campaigns/:campaignId/csv` | [docs](https://sms.cx/sms-api-documentation/#operation/ExportCampaignReportToCSV) |
| [Get Campaign Report XLSX Export](actions/get-campaign-report-xlsx-export.md) | `GET /reports/campaigns/:campaignId/xlsx` | [docs](https://sms.cx/sms-api-documentation/#operation/ExportCampaignReportToXLSX) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:conversationId` | [docs](https://sms.cx/sms-api-documentation/#operation/GetConversation) |
| [Get Conversation Read Status](actions/get-conversation-read-status.md) | `GET /conversations/:conversationId/read` | [docs](https://sms.cx/sms-api-documentation/#operation/MarkConversationAsRead) |
| [Get Number Lookup Status](actions/get-number-lookup-status.md) | `GET /numbers/lookup/lookupId/:lookupId` | [docs](https://sms.cx/sms-api-documentation/#operation/GetSingleLookupStatus) |
| [Get OTP Status](actions/get-otp-status.md) | `GET /otp/:otpId` | [docs](https://sms.cx/sms-api-documentation/#operation/GetOtpStatus) |
| [Get Report CSV Export](actions/get-report-csv-export.md) | `GET /reports/csv` | [docs](https://sms.cx/sms-api-documentation/#operation/ExportAdvancedReportToCSV) |
| [Get Report Message](actions/get-report-message.md) | `GET /reports/single/:msgId` | [docs](https://sms.cx/sms-api-documentation/#operation/GetSingleReport) |
| [Get Report Summary](actions/get-report-summary.md) | `GET /reports/summary/:dimension` | [docs](https://sms.cx/sms-api-documentation/#operation/GetSummaryReports) |
| [Get Report XLSX Export](actions/get-report-xlsx-export.md) | `GET /reports/xlsx` | [docs](https://sms.cx/sms-api-documentation/#operation/ExportAdvancedReportToXLSX) |
| [List Bulk Lookup Campaigns](actions/list-bulk-lookup-campaigns.md) | `GET /numbers/lookup` | [docs](https://sms.cx/sms-api-documentation/#operation/GetBulkLookupCampaigns) |
| [List Campaign Reports](actions/list-campaign-reports.md) | `GET /reports/campaigns` | [docs](https://sms.cx/sms-api-documentation/#operation/GetCampaignsList) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://sms.cx/sms-api-documentation/#operation/GetConverstionsList) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://sms.cx/sms-api-documentation/#operation/GetGroupsList) |
| [List Optouts](actions/list-optouts.md) | `GET /optouts` | [docs](https://sms.cx/sms-api-documentation/#operation/GetOptoutsList) |
| [List Originators](actions/list-originators.md) | `GET /originators` | [docs](https://sms.cx/sms-api-documentation/#operation/GetOriginatorsList) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://sms.cx/sms-api-documentation/#operation/GetTemplatesList) |
| [Lookup Numbers In Bulk](actions/lookup-numbers-in-bulk.md) | `POST /numbers/lookup` | [docs](https://sms.cx/sms-api-documentation/#operation/LookupNumbers) |
| [Lookup Single Number](actions/lookup-single-number.md) | `GET /numbers/lookup/:phoneNumber` | [docs](https://sms.cx/sms-api-documentation/#operation/LookupNumber) |
| [Send SMS](actions/send-sms.md) | `POST /sms` | [docs](https://sms.cx/sms-api-documentation/#operation/SendSms) |
| [Send SMS In Conversation](actions/send-sms-in-conversation.md) | `POST /conversations/:conversationId/sms` | [docs](https://sms.cx/sms-api-documentation/#operation/SendConversationReplySms) |
| [Send Viber In Conversation](actions/send-viber-in-conversation.md) | `POST /conversations/:conversationId/viber` | [docs](https://sms.cx/sms-api-documentation/#operation/SendConversationReplyViber) |
| [Send WhatsApp In Conversation](actions/send-whatsapp-in-conversation.md) | `POST /conversations/:conversationId/whatsapp` | [docs](https://sms.cx/sms-api-documentation/#operation/SendConversationReplyWhatsapp) |
| [Validate Number](actions/validate-number.md) | `GET /numbers/validate/:phoneNumber` | [docs](https://sms.cx/sms-api-documentation/#operation/ValidateNumber) |
| [Verify OTP](actions/verify-otp.md) | `POST /otp/:otpId` | [docs](https://sms.cx/sms-api-documentation/#operation/VerifyPin) |
