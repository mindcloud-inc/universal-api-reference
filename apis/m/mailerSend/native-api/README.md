# MailerSend: Native API Reference

A consolidated summary of MailerSend's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://developers.mailersend.com/api/v1/
- **OpenAPI specification:** https://api.swaggerhub.com/apis/MailerSend/mailersend-api/1.0.0-oas3.1?resolved=true
- **API base URL:** `https://api.mailersend.com/v1`

## Authentication

### API Token

Use a MailerSend API token. Requests are authenticated with an Authorization header using Bearer {{credentials.apiKey}}.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.mailersend.com/general.html)

## API conventions

Response data is read from `data`. The next-page cursor is read from `links.next`. The current page number is read from `meta.current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 10–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Domain](actions/add-domain.md) | `POST /domains` | [docs](https://developers.mailersend.com/api/v1/domains#add-a-domain) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.mailersend.com/api/v1/webhooks#create-a-webhook) |
| [Delete Domain](actions/delete-domain.md) | `DELETE /domains/:domain_id` | [docs](https://developers.mailersend.com/api/v1/domains#delete-a-domain) |
| [Delete Sender Identity](actions/delete-sender-identity.md) | `DELETE /identities/:identity_id` | [docs](https://developers.mailersend.com/api/v1/sender-identity#delete-a-sender-identity) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhook_id` | [docs](https://developers.mailersend.com/api/v1/webhooks#delete-a-webhook) |
| [Get Activity](actions/get-activity.md) | `GET /activities/:activity_id` | [docs](https://developers.mailersend.com/api/v1/activity#get-a-single-activity) |
| [Get Analytics By Country](actions/get-analytics-by-country.md) | `GET /analytics/country` | [docs](https://developers.mailersend.com/api/v1/analytics#opens-by-country) |
| [Get Analytics By Date](actions/get-analytics-by-date.md) | `GET /analytics/date` | [docs](https://developers.mailersend.com/api/v1/analytics#activity-data-by-date) |
| [Get Bulk Email Status](actions/get-bulk-email-status.md) | `GET /bulk-email/:bulk_email_id` | [docs](https://developers.mailersend.com/api/v1/email#get-bulk-email-status) |
| [Get Domain](actions/get-domain.md) | `GET /domains/:domain_id` | [docs](https://developers.mailersend.com/api/v1/domains#get-a-single-domain) |
| [Get Domain DNS Records](actions/get-domain-dns-records.md) | `GET /domains/:domain_id/dns-records` | [docs](https://developers.mailersend.com/api/v1/domains#get-dns-records) |
| [Get Domain Verification Status](actions/get-domain-verification-status.md) | `GET /domains/:domain_id/verify` | [docs](https://developers.mailersend.com/api/v1/domains#get-verification-status) |
| [Get Message](actions/get-message.md) | `GET /messages/:message_id` | [docs](https://developers.mailersend.com/api/v1/messages#get-information-for-a-single-message) |
| [Get Recipient](actions/get-recipient.md) | `GET /recipients/:recipient_id` | [docs](https://developers.mailersend.com/api/v1/recipients#get-a-single-recipient) |
| [Get Sender Identity](actions/get-sender-identity.md) | `GET /identities/:identity_id` | [docs](https://developers.mailersend.com/api/v1/sender-identity#get-a-single-sender-identity) |
| [Get Template](actions/get-template.md) | `GET /templates/:template_id` | [docs](https://developers.mailersend.com/api/v1/templates#get-a-single-template) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:webhook_id` | [docs](https://developers.mailersend.com/api/v1/webhooks#get-a-webhook) |
| [List Activity](actions/list-activity.md) | `GET /activity/:domain_id` | [docs](https://developers.mailersend.com/api/v1/activity#get-a-list-of-activities) |
| [List Domain Recipients](actions/list-domain-recipients.md) | `GET /domains/:domain_id/recipients` | [docs](https://developers.mailersend.com/api/v1/domains#get-recipients-for-a-domain) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://developers.mailersend.com/api/v1/domains#get-a-list-of-domains) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://developers.mailersend.com/api/v1/messages#get-a-list-of-messages) |
| [List Recipients](actions/list-recipients.md) | `GET /recipients` | [docs](https://developers.mailersend.com/api/v1/recipients#get-recipients) |
| [List Sender Identities](actions/list-sender-identities.md) | `GET /identities` | [docs](https://developers.mailersend.com/api/v1/sender-identity#get-a-list-of-sender-identities) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.mailersend.com/api/v1/templates#get-templates) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.mailersend.com/api/v1/webhooks#get-a-list-of-webhooks) |
| [Send Email](actions/send-email.md) | `POST /email` | [docs](https://developers.mailersend.com/api/v1/email#send-an-email) |
| [Update Sender Identity](actions/update-sender-identity.md) | `PUT /identities/:identity_id` | [docs](https://developers.mailersend.com/api/v1/sender-identity#update-a-sender-identity) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:webhook_id` | [docs](https://developers.mailersend.com/api/v1/webhooks#update-a-webhook) |
