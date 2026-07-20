# <img src="https://images.mindcloud.co/apps/icons/turbo-smtp_1775139667914.png" alt="turboSMTP logo" width="28" height="28"> turboSMTP: Universal API

turboSMTP is an email delivery platform with APIs for sending transactional email, suppressions, analytics, alerts, billing, email validation, and subaccount management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/turboSMTP/latest
- **Category:** Communication / Email Communications
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://serversmtp.com
- **Vendor API docs:** https://serversmtp.com/turbo-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Countries](actions/list-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Create Alert](actions/create-alert.md) | POST | Creates a new alert in turboSMTP. |
| [Delete Alert](actions/delete-alert.md) | DELETE | Deletes an existing alert from turboSMTP. |
| [Get Alert](actions/get-alert.md) | GET | Retrieves an alert from your turboSMTP account. |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves alerts from your turboSMTP account. |
| [Update Alert](actions/update-alert.md) | PUT | Updates an existing alert in turboSMTP. |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [List Consumer Keys](actions/list-consumer-keys.md) | GET | Retrieves consumer keys from your turboSMTP account. |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Details](actions/get-billing-details.md) | GET | Retrieves personal billing details from turboSMTP. |
| [Update Billing Details](actions/update-billing-details.md) | PUT | Updates personal billing details in turboSMTP. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Billing Contact](actions/create-billing-contact.md) | POST | Creates a new billing contact in turboSMTP. |
| [List Billing Contacts](actions/list-billing-contacts.md) | GET | Retrieves billing contacts from your turboSMTP account. |
| [Update Billing Contact](actions/update-billing-contact.md) | PUT | Updates an existing billing contact in turboSMTP. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Suppressions](actions/bulk-delete-suppressions.md) | DELETE | Deletes suppressions in bulk from turboSMTP. |
| [Filter Suppressions](actions/filter-suppressions.md) | GET | Finds suppressions in turboSMTP by custom filters. |
| [Import Suppressions](actions/import-suppressions.md) | POST | Imports email suppressions into your turboSMTP account. |
| [List Suppressions](actions/list-suppressions.md) | GET | Retrieves email suppressions from your turboSMTP account. |
| [List Validated Emails by List](actions/list-validated-emails-by-list.md) | GET | Retrieves validated emails from a turboSMTP validation list. |
| [Send Email](actions/send-email.md) | POST | Sends an email message with turboSMTP. |
| [Validate Email](actions/validate-email.md) | POST | Validates an email address in turboSMTP. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Validation List Summary](actions/get-email-validation-list-summary.md) | GET | Retrieves an email validation list summary from turboSMTP. |
| [List Email Validation Lists](actions/list-email-validation-lists.md) | GET | Retrieves email validation lists from turboSMTP. |
| [Upload Email Validation File](actions/upload-email-validation-file.md) | POST | Uploads a file for email validation in turboSMTP. |
| [Validate Email Validation List](actions/validate-email-validation-list.md) | PUT | Validates an email validation list in turboSMTP. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves available countries from your turboSMTP account. |
| [List States by Country](actions/list-states-by-country.md) | GET | Retrieves states for a country from turboSMTP. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics Item](actions/get-analytics-item.md) | GET | Retrieves an analytics item from turboSMTP. |
| [List Analytics Data](actions/list-analytics-data.md) | GET | Retrieves email analytics data from turboSMTP. |

### Subaccount

| Action | Method | Description |
| --- | --- | --- |
| [Check If Account Email Exists](actions/check-if-account-email-exists.md) | GET | Checks whether an account email exists in turboSMTP. |
| [List Subaccounts](actions/list-subaccounts.md) | GET | Retrieves subaccounts from your turboSMTP account. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Validation Subscription](actions/get-email-validation-subscription.md) | GET | Retrieves email validation subscription details from turboSMTP. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves your turboSMTP user account details. |

