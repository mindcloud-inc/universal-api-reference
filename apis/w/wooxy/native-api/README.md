# Wooxy: Native API Reference

A consolidated summary of Wooxy's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://wooxy.com/api-documentation
- **API base URL:** `https://api.wooxy.com`

## Authentication

### Access-Token

Send the Wooxy API secret in the Access-Token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Access-Token: <apiKey>
```

[Official authentication documentation](https://wooxy.com/knowledge-base/your-account/security)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request body to set the page size (default 20). Use `offset` in the request body as the record offset.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account Variable](actions/create-account-variable.md) | `POST v3/global-variables/create` | [docs](https://wooxy.com/api-documentation/variables/create-account-variable) |
| [Create Contact](actions/create-contact.md) | `POST v3/contacts/add` | [docs](https://wooxy.com/api-documentation/contacts/add-new-contact) |
| [Create Contact List Variable](actions/create-contact-list-variable.md) | `POST v3/contact-list/variables/add` | [docs](https://wooxy.com/api-documentation/contact-list/add-contact-list-variable) |
| [Create Domain](actions/create-domain.md) | `POST v3/domain/create` | [docs](https://wooxy.com/api-documentation/domains/create-domain) |
| [Create Event](actions/create-event.md) | `POST v3/custom-event/create` | [docs](https://wooxy.com/api-documentation/events/create-event) |
| [Create Tag](actions/create-tag.md) | `POST v3/tags/create` | [docs](https://wooxy.com/api-documentation/tags/create-tag) |
| [Create Template](actions/create-template.md) | `POST v3/template/email/create` | [docs](https://wooxy.com/api-documentation/templates/create-template) |
| [Create Webhook](actions/create-webhook.md) | `POST v3/webhook/create` | [docs](https://wooxy.com/api-documentation/webhooks/webhook-create) |
| [Delete Account Variable](actions/delete-account-variable.md) | `POST v3/global-variables/remove` | [docs](https://wooxy.com/api-documentation/variables/remove-account-variable) |
| [Delete Contact](actions/delete-contact.md) | `POST v3/contacts/remove` | [docs](https://wooxy.com/api-documentation/contacts/remove-contact) |
| [Delete Domain](actions/delete-domain.md) | `POST v3/domain/remove` | [docs](https://wooxy.com/api-documentation/domains/remove-domain) |
| [Delete Event](actions/delete-event.md) | `POST v3/custom-event/remove` | [docs](https://wooxy.com/api-documentation/events/remove-event) |
| [Delete Tag](actions/delete-tag.md) | `POST v3/tags/remove` | [docs](https://wooxy.com/api-documentation/tags/remove-tag) |
| [Delete Template](actions/delete-template.md) | `POST v3/template/email/remove` | [docs](https://wooxy.com/api-documentation/templates/remove-template) |
| [Delete Webhook](actions/delete-webhook.md) | `POST v3/webhook/remove` | [docs](https://wooxy.com/api-documentation/webhooks/webhook-remove) |
| [Fire Event](actions/fire-event.md) | `POST v3/custom-event/fire` | [docs](https://wooxy.com/api-documentation/events/fire-event) |
| [Get Account Info](actions/get-account-info.md) | `POST v3/account/info` | [docs](https://wooxy.com/api-documentation/account/get-account-info) |
| [Get Contact](actions/get-contact.md) | `POST v3/contact/get` | [docs](https://wooxy.com/api-documentation/contacts/get-contact) |
| [Get Contact List](actions/get-contact-list.md) | `POST v3/contact-list/get` | [docs](https://wooxy.com/api-documentation/contact-list/get-contact-list) |
| [Get Contact Mutation Request Status](actions/get-contact-mutation-request-status.md) | `POST v3/request/find` | [docs](https://wooxy.com/api-documentation/contacts/get-add-update-remove-request-status) |
| [Get Domain](actions/get-domain.md) | `POST v3/domain/get` | [docs](https://wooxy.com/api-documentation/domains/get-domain) |
| [Get Event](actions/get-event.md) | `POST v3/custom-event/get` | [docs](https://wooxy.com/api-documentation/events/get-event) |
| [Get Message Statistics](actions/get-message-statistics.md) | `POST v3/mailer/info` | [docs](https://wooxy.com/api-documentation/email/get-message-statistics) |
| [Get Tag](actions/get-tag.md) | `POST v3/tags/get` | [docs](https://wooxy.com/api-documentation/tags/get-tag) |
| [Get Template](actions/get-template.md) | `POST v3/template/email/get` | [docs](https://wooxy.com/api-documentation/templates/get-template) |
| [List Account Variables](actions/list-account-variables.md) | `POST v3/global-variables/find` | [docs](https://wooxy.com/api-documentation/variables/get-account-variables) |
| [List Contact Lists](actions/list-contact-lists.md) | `POST v3/contact-list/find` | [docs](https://wooxy.com/api-documentation/contact-list/find-contact-list) |
| [List Domains](actions/list-domains.md) | `POST v3/domain/find` | [docs](https://wooxy.com/api-documentation/domains/find-domain) |
| [List Events](actions/list-events.md) | `POST v3/custom-event/find` | [docs](https://wooxy.com/api-documentation/events/find-event) |
| [List Templates](actions/list-templates.md) | `POST v3/template/email/find` | [docs](https://wooxy.com/api-documentation/templates/find-template) |
| [List Webhooks](actions/list-webhooks.md) | `POST v3/webhook/list` | [docs](https://wooxy.com/api-documentation/webhooks/get-webhook-list) |
| [Send Batch Email](actions/send-batch-email.md) | `POST v3/mailer/batch-send` | [docs](https://wooxy.com/api-documentation/email/send-batch-email) |
| [Send Batch Triggered Email](actions/send-batch-triggered-email.md) | `POST v3/mailer/batch-trigger` | [docs](https://wooxy.com/api-documentation/email/send-batch-triggered-email) |
| [Send Email](actions/send-email.md) | `POST v3/mailer/send` | [docs](https://wooxy.com/api-documentation/email/send-email) |
| [Send Triggered Email](actions/send-triggered-email.md) | `POST v3/mailer/trigger` | [docs](https://wooxy.com/api-documentation/email/send-triggered-email) |
| [Update Account Variable](actions/update-account-variable.md) | `POST v3/global-variables/update` | [docs](https://wooxy.com/api-documentation/variables/update-account-variable) |
| [Update Contact](actions/update-contact.md) | `POST v3/contacts/update` | [docs](https://wooxy.com/api-documentation/contacts/update-contact-data) |
| [Update Event](actions/update-event.md) | `POST v3/custom-event/update` | [docs](https://wooxy.com/api-documentation/events/update-event) |
| [Update Tag](actions/update-tag.md) | `POST v3/tags/update` | [docs](https://wooxy.com/api-documentation/tags/update-tag) |
| [Update Template](actions/update-template.md) | `POST v3/template/email/update` | [docs](https://wooxy.com/api-documentation/templates/update-template) |
| [Verify Domain](actions/verify-domain.md) | `POST v3/domain/verify` | [docs](https://wooxy.com/api-documentation/domains/verify-domain) |
