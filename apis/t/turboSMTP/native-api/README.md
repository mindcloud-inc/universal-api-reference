# turboSMTP: Native API Reference

A consolidated summary of turboSMTP's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://serversmtp.com/turbo-api/
- **OpenAPI specification:** https://serversmtp.com/turbo-api/turbo-smtp.yaml
- **API base URL:** `https://pro.api.serversmtp.com/api/v2`

## Authentication

### Consumer Key + Consumer Secret

Use turboSMTP API Keys from Settings > Integrations > API Keys. The Consumer Secret is only shown once when the key is generated.

### Credentials

- **Consumer Key:** `consumerKey` · required · turboSMTP API key consumer key.
- **Consumer Secret:** `consumerSecret` · required · turboSMTP API key consumer secret.

Send these headers with each API request:

```http
consumerKey: <consumerKey>
consumerSecret: <consumerSecret>
```

[Official authentication documentation](https://serversmtp.com/turbo-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Delete Suppressions](actions/bulk-delete-suppressions.md) | `POST /suppressions/bulk_delete` | [docs](https://serversmtp.com/turbo-api/#/suppressions/bulkDeleteSuppressions) |
| [Check If Account Email Exists](actions/check-if-account-email-exists.md) | `GET /subaccounts/email-exists` | [docs](https://serversmtp.com/turbo-api/#/subaccounts/checkIfAccountEmailExists) |
| [Create Alert](actions/create-alert.md) | `POST /tools/alerts` | [docs](https://serversmtp.com/turbo-api/#/alerts/createAlert) |
| [Create Billing Contact](actions/create-billing-contact.md) | `POST /billing/contacts` |  |
| [Delete Alert](actions/delete-alert.md) | `DELETE /tools/alerts/{Id}` | [docs](https://serversmtp.com/turbo-api/#/alerts/deleteAlert) |
| [Filter Suppressions](actions/filter-suppressions.md) | `POST /suppressions` | [docs](https://serversmtp.com/turbo-api/#/suppressions/filterSuppressions) |
| [Get Alert](actions/get-alert.md) | `GET /tools/alerts/{Id}` | [docs](https://serversmtp.com/turbo-api/#/alerts/getAlert) |
| [Get Analytics Item](actions/get-analytics-item.md) | `GET /analytics/{Id}` | [docs](https://serversmtp.com/turbo-api/#/analytics/getAnalyticsDataByID) |
| [Get Billing Details](actions/get-billing-details.md) | `GET /billing/details` |  |
| [Get Email Validation List Summary](actions/get-email-validation-list-summary.md) | `GET /emailvalidation/lists/{Id}` | [docs](https://serversmtp.com/turbo-api/#/email-validator/getEmailValidationListSummary) |
| [Get Email Validation Subscription](actions/get-email-validation-subscription.md) | `GET /emailvalidation/subscription` | [docs](https://serversmtp.com/turbo-api/#/email-validator/getEmailValidationSubscription) |
| [Get User Details](actions/get-user-details.md) | `GET /user` |  |
| [Import Suppressions](actions/import-suppressions.md) | `POST /suppressions/import` | [docs](https://serversmtp.com/turbo-api/#/suppressions/importSuppressions) |
| [List Alerts](actions/list-alerts.md) | `GET /tools/alerts` | [docs](https://serversmtp.com/turbo-api/#/alerts/getAlerts) |
| [List Analytics Data](actions/list-analytics-data.md) | `GET /analytics` | [docs](https://serversmtp.com/turbo-api/#/analytics/getAnalyticsData) |
| [List Billing Contacts](actions/list-billing-contacts.md) | `GET /billing/contacts` |  |
| [List Consumer Keys](actions/list-consumer-keys.md) | `GET /user/consumerKeys` | [docs](https://serversmtp.com/turbo-api/#/consumerkey/listConsumerKeys) |
| [List Countries](actions/list-countries.md) | `GET /meta/countries` | [docs](https://serversmtp.com/turbo-api/#/meta/getCountries) |
| [List Email Validation Lists](actions/list-email-validation-lists.md) | `GET /emailvalidation/lists` | [docs](https://serversmtp.com/turbo-api/#/email-validator/getEmailValidationLists) |
| [List States by Country](actions/list-states-by-country.md) | `GET /meta/state/{isoCode}` | [docs](https://serversmtp.com/turbo-api/#/meta/getStatesByCountry) |
| [List Subaccounts](actions/list-subaccounts.md) | `GET /subaccounts/list` | [docs](https://serversmtp.com/turbo-api/#/subaccounts/getSubaccounts) |
| [List Suppressions](actions/list-suppressions.md) | `GET /suppressions` | [docs](https://serversmtp.com/turbo-api/#/suppressions/getSuppressions) |
| [List Validated Emails by List](actions/list-validated-emails-by-list.md) | `GET /emailvalidation/lists/{Id}/emails` | [docs](https://serversmtp.com/turbo-api/#/email-validator/getValidatedEmailsByList) |
| [Send Email](actions/send-email.md) | `POST /mail/send` | [docs](https://serversmtp.com/turbo-api/#/mail/sendEmail) |
| [Update Alert](actions/update-alert.md) | `PATCH /tools/alerts/{Id}` | [docs](https://serversmtp.com/turbo-api/#/alerts/updateAlert) |
| [Update Billing Contact](actions/update-billing-contact.md) | `PUT /billing/contacts/{Id}` |  |
| [Update Billing Details](actions/update-billing-details.md) | `PUT /billing/details` |  |
| [Upload Email Validation File](actions/upload-email-validation-file.md) | `POST /emailvalidation/upload` | [docs](https://serversmtp.com/turbo-api/#/email-validator/uploadEmailValidationFile) |
| [Validate Email](actions/validate-email.md) | `POST /emailvalidation/validateEmail` | [docs](https://serversmtp.com/turbo-api/#/email-validator/validateEmail) |
| [Validate Email Validation List](actions/validate-email-validation-list.md) | `POST /emailvalidation/lists/{Id}/validate` | [docs](https://serversmtp.com/turbo-api/#/email-validator/validateEmailValidatorList) |
