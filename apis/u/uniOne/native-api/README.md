# UniOne: Native API Reference

A consolidated summary of UniOne's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.unione.io/en/web-api-ref
- **API base URL:** `https://api.unione.io/en/transactional/api/v1`

## Authentication

### API Key

Authenticate to the UniOne Web API with the X-API-KEY request header.

[Official authentication documentation](https://docs.unione.io/en/web-api-ref#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request body to set the page size (default 50). Use `offset` in the request body as the record offset.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Suppression](actions/add-suppression.md) | `POST suppression/set.json` | [docs](https://docs.unione.io/en/web-api-ref#suppression-set) |
| [Check Unsubscribed](actions/check-unsubscribed.md) | `POST unsubscribed/check.json` | [docs](https://docs.unione.io/en/web-api-ref#unsubscribed-check) |
| [Create Event Dump Job](actions/create-event-dump-job.md) | `POST event-dump/create.json` | [docs](https://docs.unione.io/en/web-api-ref#event-dump-create) |
| [Create Or Update Template](actions/create-or-update-template.md) | `POST template/set.json` | [docs](https://docs.unione.io/en/web-api-ref#template-set) |
| [Create Or Update Webhook](actions/create-or-update-webhook.md) | `POST webhook/set.json` | [docs](https://docs.unione.io/en/web-api-ref#webhook-set) |
| [Create Project](actions/create-project.md) | `POST project/create.json` | [docs](https://docs.unione.io/en/web-api-ref#project-create) |
| [Delete Domain](actions/delete-domain.md) | `POST domain/delete.json` | [docs](https://docs.unione.io/en/web-api-ref#domain-delete) |
| [Delete Event Dump Job](actions/delete-event-dump-job.md) | `POST event-dump/delete.json` | [docs](https://docs.unione.io/en/web-api-ref#event-dump-delete) |
| [Delete Project](actions/delete-project.md) | `POST project/delete.json` | [docs](https://docs.unione.io/en/web-api-ref#project-delete) |
| [Delete Suppression](actions/delete-suppression.md) | `POST suppression/delete.json` | [docs](https://docs.unione.io/en/web-api-ref#suppression-delete) |
| [Delete Tag](actions/delete-tag.md) | `POST tag/delete.json` | [docs](https://docs.unione.io/en/web-api-ref#tag-delete) |
| [Delete Template](actions/delete-template.md) | `POST template/delete.json` | [docs](https://docs.unione.io/en/web-api-ref#template-delete) |
| [Delete Webhook](actions/delete-webhook.md) | `POST webhook/delete.json` | [docs](https://docs.unione.io/en/web-api-ref#webhook-delete) |
| [Get Domain DNS Records](actions/get-domain-dns-records.md) | `POST domain/get-dns-records.json` | [docs](https://docs.unione.io/en/web-api-ref#domain-get-dns-records) |
| [Get Event Dump Job](actions/get-event-dump-job.md) | `POST event-dump/get.json` | [docs](https://docs.unione.io/en/web-api-ref#event-dump-get) |
| [Get Suppression](actions/get-suppression.md) | `POST suppression/get.json` | [docs](https://docs.unione.io/en/web-api-ref#suppression-get) |
| [Get System Info](actions/get-system-info.md) | `POST system/info.json` | [docs](https://docs.unione.io/en/web-api-ref#system-info) |
| [Get Template](actions/get-template.md) | `POST template/get.json` | [docs](https://docs.unione.io/en/web-api-ref#template-get) |
| [Get Webhook](actions/get-webhook.md) | `POST webhook/get.json` | [docs](https://docs.unione.io/en/web-api-ref#webhook-get) |
| [List Domains](actions/list-domains.md) | `POST domain/list.json` | [docs](https://docs.unione.io/en/web-api-ref#domain-list) |
| [List Event Dump Jobs](actions/list-event-dump-jobs.md) | `POST event-dump/list.json` | [docs](https://docs.unione.io/en/web-api-ref#event-dump-list) |
| [List Projects](actions/list-projects.md) | `POST project/list.json` | [docs](https://docs.unione.io/en/web-api-ref#project-list) |
| [List Suppressions](actions/list-suppressions.md) | `POST suppression/list.json` | [docs](https://docs.unione.io/en/web-api-ref#suppression-list) |
| [List Tags](actions/list-tags.md) | `POST tag/list.json` | [docs](https://docs.unione.io/en/web-api-ref#tag-list) |
| [List Templates](actions/list-templates.md) | `POST template/list.json` | [docs](https://docs.unione.io/en/web-api-ref#template-list) |
| [List Unsubscribed](actions/list-unsubscribed.md) | `POST unsubscribed/list.json` | [docs](https://docs.unione.io/en/web-api-ref#unsubscribed-list) |
| [List Webhooks](actions/list-webhooks.md) | `POST webhook/list.json` | [docs](https://docs.unione.io/en/web-api-ref#webhook-list) |
| [Send Email](actions/send-email.md) | `POST email/send.json` | [docs](https://docs.unione.io/en/web-api-ref#email-send) |
| [Set Unsubscribed](actions/set-unsubscribed.md) | `POST unsubscribed/set.json` | [docs](https://docs.unione.io/en/web-api-ref#unsubscribed-set) |
| [Subscribe Email](actions/subscribe-email.md) | `POST email/subscribe.json` | [docs](https://docs.unione.io/en/web-api-ref#email-subscribe) |
| [Update Project](actions/update-project.md) | `POST project/update.json` | [docs](https://docs.unione.io/en/web-api-ref#project-update) |
| [Validate DKIM](actions/validate-dkim.md) | `POST domain/validate-dkim.json` | [docs](https://docs.unione.io/en/web-api-ref#domain-validate-dkim) |
| [Validate Domain Verification Record](actions/validate-domain-verification-record.md) | `POST domain/validate-verification-record.json` | [docs](https://docs.unione.io/en/web-api-ref#domain-validate-verification-record) |
| [Validate Single Email](actions/validate-single-email.md) | `POST email-validation/single.json` | [docs](https://docs.unione.io/en/web-api-ref#email-validation-single) |
