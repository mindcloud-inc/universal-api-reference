# Fingertip: Native API Reference

A consolidated summary of Fingertip's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://docs.fingertip.com/rest-api
- **API base URL:** `https://api.fingertip.com`

## Authentication

### API Key

Authenticate Fingertip requests with a Bearer API key from fingertip.com/api-keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.fingertip.com/node-sdk)

## API conventions

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 10; maximum 25). Use `cursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortDirection`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Block](actions/create-block.md) | `POST /v1/pages/:pageId/blocks` | [docs](https://docs.fingertip.com/openapi-specs/create-block) |
| [Create Page](actions/create-page.md) | `POST /v1/sites/:siteId/pages` | [docs](https://docs.fingertip.com/openapi-specs/create-page) |
| [Create Site](actions/create-site.md) | `POST /v1/sites` | [docs](https://docs.fingertip.com/openapi-specs/create-site) |
| [Create Site Contact](actions/create-site-contact.md) | `POST /v1/site-contacts` | [docs](https://docs.fingertip.com/openapi-specs/create-site-contact.md) |
| [Create Site Membership](actions/create-site-membership.md) | `POST /v1/sites/:siteId/memberships` | [docs](https://docs.fingertip.com/openapi-specs/create-site-membership.md) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhooks` | [docs](https://docs.fingertip.com/openapi-specs/create-webhook.md) |
| [Delete Page](actions/delete-page.md) | `DELETE /v1/pages/:pageId` | [docs](https://docs.fingertip.com/openapi-specs/delete-page) |
| [Delete Site](actions/delete-site.md) | `DELETE /v1/sites/:siteId` | [docs](https://docs.fingertip.com/openapi-specs/delete-site) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/:webhookId` | [docs](https://docs.fingertip.com/openapi-specs/delete-webhook.md) |
| [Get Blog Post](actions/get-blog-post.md) | `GET /v1/blog-posts/:blogPostId` | [docs](https://docs.fingertip.com/openapi-specs/get-blog-post.md) |
| [Get Event Type](actions/get-event-type.md) | `GET /v1/event-types/:eventTypeId` | [docs](https://docs.fingertip.com/openapi-specs/get-event-type.md) |
| [Get Form Template](actions/get-form-template.md) | `GET /v1/form-templates/:formTemplateId` | [docs](https://docs.fingertip.com/openapi-specs/get-form-template.md) |
| [Get Health Check](actions/get-health-check.md) | `GET /v1/ping` | [docs](https://docs.fingertip.com/openapi-specs/health-check-endpoint) |
| [Get Page](actions/get-page.md) | `GET /v1/pages/:pageId` | [docs](https://docs.fingertip.com/openapi-specs/get-page) |
| [Get Page Theme](actions/get-page-theme.md) | `GET /v1/pages/:pageId/theme` | [docs](https://docs.fingertip.com/openapi-specs/get-page-theme) |
| [Get Site](actions/get-site.md) | `GET /v1/sites/:siteId` | [docs](https://docs.fingertip.com/openapi-specs/get-site) |
| [Get Site Analytics](actions/get-site-analytics.md) | `GET /v1/sites/:siteId/analytics` | [docs](https://docs.fingertip.com/openapi-specs/get-comprehensive-site-analytics) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/:webhookId` | [docs](https://docs.fingertip.com/openapi-specs/get-webhook.md) |
| [Get Workspace](actions/get-workspace.md) | `GET /v1/workspaces/:workspaceId` | [docs](https://docs.fingertip.com/openapi-specs/get-workspace.md) |
| [List Blocks](actions/list-blocks.md) | `GET /v1/pages/:pageId/blocks` | [docs](https://docs.fingertip.com/openapi-specs/list-blocks) |
| [List Blog Posts](actions/list-blog-posts.md) | `GET /v1/blog-posts` | [docs](https://docs.fingertip.com/openapi-specs/list-blog-posts.md) |
| [List Bookings](actions/list-bookings.md) | `GET /v1/bookings` | [docs](https://docs.fingertip.com/openapi-specs/list-bookings.md) |
| [List Event Types](actions/list-event-types.md) | `GET /v1/event-types` | [docs](https://docs.fingertip.com/openapi-specs/list-event-types.md) |
| [List Form Responses](actions/list-form-responses.md) | `GET /v1/form-responses` | [docs](https://docs.fingertip.com/openapi-specs/list-form-responses.md) |
| [List Form Templates](actions/list-form-templates.md) | `GET /v1/form-templates` | [docs](https://docs.fingertip.com/openapi-specs/list-form-templates.md) |
| [List Invoices](actions/list-invoices.md) | `GET /v1/invoices` | [docs](https://docs.fingertip.com/openapi-specs/list-invoices.md) |
| [List Orders](actions/list-orders.md) | `GET /v1/orders` | [docs](https://docs.fingertip.com/openapi-specs/list-orders.md) |
| [List Pages](actions/list-pages.md) | `GET /v1/sites/:siteId/pages` | [docs](https://docs.fingertip.com/openapi-specs/list-pages) |
| [List Site Contacts](actions/list-site-contacts.md) | `GET /v1/site-contacts` | [docs](https://docs.fingertip.com/openapi-specs/list-site-contacts.md) |
| [List Site Memberships](actions/list-site-memberships.md) | `GET /v1/sites/:siteId/memberships` | [docs](https://docs.fingertip.com/openapi-specs/list-site-memberships.md) |
| [List Sites](actions/list-sites.md) | `GET /v1/sites` | [docs](https://docs.fingertip.com/openapi-specs/list-sites) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://docs.fingertip.com/openapi-specs/list-webhooks.md) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/workspaces` | [docs](https://docs.fingertip.com/openapi-specs/list-workspaces.md) |
| [Update Page](actions/update-page.md) | `PATCH /v1/pages/:pageId` | [docs](https://docs.fingertip.com/openapi-specs/update-page) |
| [Update Page Theme](actions/update-page-theme.md) | `PATCH /v1/pages/:pageId/theme` | [docs](https://docs.fingertip.com/openapi-specs/update-page-theme) |
| [Update Site](actions/update-site.md) | `PATCH /v1/sites/:siteId` | [docs](https://docs.fingertip.com/openapi-specs/update-site) |
| [Update Site Membership](actions/update-site-membership.md) | `PATCH /v1/site-memberships/:membershipId` | [docs](https://docs.fingertip.com/openapi-specs/update-site-membership.md) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /v1/webhooks/:webhookId` | [docs](https://docs.fingertip.com/openapi-specs/update-webhook.md) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /v1/workspaces/:workspaceId` | [docs](https://docs.fingertip.com/openapi-specs/update-workspace.md) |
