# ActiveCampaign: Native API Reference

A consolidated summary of ActiveCampaign's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://developers.activecampaign.com/reference/overview
- **OpenAPI specification:** https://developers.activecampaign.com/openapi/v3.json
- **API base URL:** `{apiUrl}/api/3`

## Authentication

### API Key

Authenticate with ActiveCampaign API key sent in the Api-Token header.

### Credentials

- **API Key:** `apiKey` · required
- **API URL:** `apiUrl` · required · Your ActiveCampaign account API URL from Settings > Developer (for example https://youraccount.api-us1.com). Do not include /api/3.

Send these headers with each API request:

```http
Api-Token: <apiKey>
```

[Official authentication documentation](https://developers.activecampaign.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`, `neq`, `starts_with`.

## Sorting

Set the sort field with `orders` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact To Automation](actions/add-contact-to-automation.md) | `POST /contactAutomations` | [docs](https://developers.activecampaign.com/reference/create-new-contactautomation) |
| [Add Tag To Contact](actions/add-tag-to-contact.md) | `POST /contactTags` | [docs](https://developers.activecampaign.com/reference/create-contact-tag) |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://developers.activecampaign.com/reference/create-an-account-new) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.activecampaign.com/reference/create-a-new-contact) |
| [Create Custom Field Value](actions/create-custom-field-value.md) | `POST /fieldValues` | [docs](https://developers.activecampaign.com/reference/create-fieldvalue) |
| [Create Deal](actions/create-deal.md) | `POST /deals` | [docs](https://developers.activecampaign.com/reference/create-a-deal-new) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://developers.activecampaign.com/reference/create-new-list) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://developers.activecampaign.com/reference/delete-contact) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /deals/:id` | [docs](https://developers.activecampaign.com/reference/delete-a-deal) |
| [Delete List](actions/delete-list.md) | `DELETE /lists/:id` | [docs](https://developers.activecampaign.com/reference/delete-a-list) |
| [Get Account](actions/get-account.md) | `GET /accounts/:id` | [docs](https://developers.activecampaign.com/reference/retrieve-an-account) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://developers.activecampaign.com/reference/get-contact) |
| [Get Deal](actions/get-deal.md) | `GET /deals/:id` | [docs](https://developers.activecampaign.com/reference/retrieve-a-deal) |
| [Get List](actions/get-list.md) | `GET /lists/:id` | [docs](https://developers.activecampaign.com/reference/retrieve-a-list) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://developers.activecampaign.com/reference/list-all-accounts) |
| [List Automations](actions/list-automations.md) | `GET /automations` | [docs](https://developers.activecampaign.com/reference/list-all-automations) |
| [List Contact Automations](actions/list-contact-automations.md) | `GET /contactAutomations` | [docs](https://developers.activecampaign.com/reference/list-all-contact-automations) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.activecampaign.com/reference/list-all-contacts) |
| [List Custom Field Values](actions/list-custom-field-values.md) | `GET /fieldValues` | [docs](https://developers.activecampaign.com/reference/list-all-custom-field-values) |
| [List Deal Stages](actions/list-deal-stages.md) | `GET /dealStages` | [docs](https://developers.activecampaign.com/reference/list-all-deal-stages) |
| [List Deals](actions/list-deals.md) | `GET /deals` | [docs](https://developers.activecampaign.com/reference/list-all-deals) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://developers.activecampaign.com/reference/retrieve-all-lists) |
| [List Pipelines](actions/list-pipelines.md) | `GET /dealGroups` | [docs](https://developers.activecampaign.com/reference/list-all-pipelines) |
| [Remove Contact From Automation](actions/remove-contact-from-automation.md) | `DELETE /contactAutomations/:id` | [docs](https://developers.activecampaign.com/reference/delete-a-contactautomation) |
| [Remove Tag From Contact](actions/remove-tag-from-contact.md) | `DELETE /contactTags/:id` | [docs](https://developers.activecampaign.com/reference/remove-a-contacts-tag) |
| [Sync Contact](actions/sync-contact.md) | `POST /contact/sync` | [docs](https://developers.activecampaign.com/reference/sync-a-contacts-data) |
| [Update Account](actions/update-account.md) | `PUT /accounts/:id` | [docs](https://developers.activecampaign.com/reference/update-an-account-new) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://developers.activecampaign.com/reference/update-a-contact-new) |
| [Update Contact List Status](actions/update-contact-list-status.md) | `POST /contactLists` | [docs](https://developers.activecampaign.com/reference/update-list-status-for-contact) |
| [Update Custom Field Value For Contact](actions/update-custom-field-value-for-contact.md) | `PUT /fieldValues/:id` | [docs](https://developers.activecampaign.com/reference/update-a-custom-field-value-for-contact) |
| [Update Deal](actions/update-deal.md) | `PUT /deals/:id` | [docs](https://developers.activecampaign.com/reference/update-a-deal-new) |
