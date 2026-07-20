# SparkPost: Native API Reference

A consolidated summary of SparkPost's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.sparkpost.com/api/
- **API base URL:** `https://api.sparkpost.com/api/v1`

## Authentication

### API Key (Header)

Authenticate SparkPost requests with a raw API key in the Authorization header.

### Credentials

- **API Key:** `apiKey` · optional · SparkPost API key used in the Authorization header.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://developers.sparkpost.com/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Tracking Domain Certificate Eligibility](actions/check-tracking-domain-certificate-eligibility.md) | `POST /tracking-domains/:domain/certificate/check` | [docs](https://developers.sparkpost.com/api/tracking-domains/#tracking-domains-post-check-certificate-eligibility) |
| [Create Recipient List](actions/create-recipient-list.md) | `POST /recipient-lists` | [docs](https://developers.sparkpost.com/api/recipient-lists/#recipient-lists-post-create-a-recipient-list) |
| [Create Sending Domain](actions/create-sending-domain.md) | `POST /sending-domains` | [docs](https://developers.sparkpost.com/api/sending-domains/#sending-domains-post-create-a-sending-domain) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://developers.sparkpost.com/api/templates/#templates-post-create-a-template) |
| [Create Tracking Domain](actions/create-tracking-domain.md) | `POST /tracking-domains` | [docs](https://developers.sparkpost.com/api/tracking-domains/#tracking-domains-post-create-a-tracking-domain) |
| [List Recipient Lists](actions/list-recipient-lists.md) | `GET /recipient-lists` | [docs](https://developers.sparkpost.com/api/recipient-lists/#recipient-lists-get-list-all-recipient-lists) |
| [List Sending Domains](actions/list-sending-domains.md) | `GET /sending-domains` | [docs](https://developers.sparkpost.com/api/sending-domains/#sending-domains-get-list-all-sending-domains) |
| [List Subaccounts](actions/list-subaccounts.md) | `GET /subaccounts` | [docs](https://developers.sparkpost.com/api/subaccounts/#subaccounts-get-list-subaccounts) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.sparkpost.com/api/templates/#templates-get-list-all-templates) |
| [List Tracking Domains](actions/list-tracking-domains.md) | `GET /tracking-domains` | [docs](https://developers.sparkpost.com/api/tracking-domains/#tracking-domains-get-list-all-tracking-domains) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.sparkpost.com/api/webhooks/#webhooks-get-list-all-webhooks) |
| [Preview Template](actions/preview-template.md) | `POST /templates/:id/preview` | [docs](https://developers.sparkpost.com/api/templates/#templates-post-preview-a-template) |
| [Retrieve Account](actions/retrieve-account.md) | `GET /account` | [docs](https://developers.sparkpost.com/api/account/#account-get-retrieve-account-information) |
| [Retrieve Recipient List](actions/retrieve-recipient-list.md) | `GET /recipient-lists/:id` | [docs](https://developers.sparkpost.com/api/recipient-lists/#recipient-lists-get-retrieve-a-recipient-list) |
| [Retrieve Sending Domain](actions/retrieve-sending-domain.md) | `GET /sending-domains/:domain` | [docs](https://developers.sparkpost.com/api/sending-domains/#sending-domains-get-retrieve-a-sending-domain) |
| [Retrieve Subaccounts Summary](actions/retrieve-subaccounts-summary.md) | `GET /subaccounts/summary` | [docs](https://developers.sparkpost.com/api/subaccounts/#subaccounts-get-retrieve-subaccounts-summary) |
| [Retrieve Suppression](actions/retrieve-suppression.md) | `GET /suppression-list/:recipient` | [docs](https://developers.sparkpost.com/api/suppression-list/#suppression-list-get-retrieve-a-suppression) |
| [Retrieve Suppression Summary](actions/retrieve-suppression-summary.md) | `GET /suppression-list/summary` | [docs](https://developers.sparkpost.com/api/suppression-list/#suppression-list-get-retrieve-summary) |
| [Retrieve Template](actions/retrieve-template.md) | `GET /templates/:id` | [docs](https://developers.sparkpost.com/api/templates/#templates-get-retrieve-a-template) |
| [Retrieve Tracking Domain](actions/retrieve-tracking-domain.md) | `GET /tracking-domains/:domain` | [docs](https://developers.sparkpost.com/api/tracking-domains/#tracking-domains-get-retrieve-a-tracking-domain) |
| [Retrieve Usage](actions/retrieve-usage.md) | `GET /usage` | [docs](https://developers.sparkpost.com/api/usage/#usage-get-retrieve-usage) |
| [Retrieve Webhook Event Documentation](actions/retrieve-webhook-event-documentation.md) | `GET /webhooks/events/documentation` | [docs](https://developers.sparkpost.com/api/webhooks/#webhooks-get-events-documentation) |
| [Retrieve Webhook Event Samples](actions/retrieve-webhook-event-samples.md) | `GET /webhooks/events/samples` | [docs](https://developers.sparkpost.com/api/webhooks/#webhooks-get-event-samples) |
| [Search Suppressions](actions/search-suppressions.md) | `GET /suppression-list` | [docs](https://developers.sparkpost.com/api/suppression-list/#suppression-list-get-search-suppressions) |
| [Update Account](actions/update-account.md) | `PUT /account` | [docs](https://developers.sparkpost.com/api/account/#account-put-update-account-information) |
| [Update Draft Template](actions/update-draft-template.md) | `PUT /templates/:id` | [docs](https://developers.sparkpost.com/api/templates/#templates-put-update-a-draft) |
| [Update Sending Domain](actions/update-sending-domain.md) | `PUT /sending-domains/:domain` | [docs](https://developers.sparkpost.com/api/sending-domains/#sending-domains-put-update-a-sending-domain) |
| [Update Tracking Domain](actions/update-tracking-domain.md) | `PUT /tracking-domains/:domain` | [docs](https://developers.sparkpost.com/api/tracking-domains/#tracking-domains-put-update-a-tracking-domain) |
| [Verify Sending Domain](actions/verify-sending-domain.md) | `POST /sending-domains/:domain/verify` | [docs](https://developers.sparkpost.com/api/sending-domains/#sending-domains-post-verify-a-sending-domain) |
| [Verify Tracking Domain](actions/verify-tracking-domain.md) | `POST /tracking-domains/:domain/verify` | [docs](https://developers.sparkpost.com/api/tracking-domains/#tracking-domains-post-verify-a-tracking-domain) |
