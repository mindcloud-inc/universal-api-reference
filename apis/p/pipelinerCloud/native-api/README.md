# Pipeliner Cloud: Native API Reference

A consolidated summary of Pipeliner Cloud's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://pipelinercrm.eu.apidog.com/
- **OpenAPI specification:** http://pipeliner-api-doc.s3-website-eu-west-1.amazonaws.com/latest/rest/space/openapi.json
- **API base URL:** `{serviceUrl}/api/v100/rest/spaces/{spaceId}`

## Authentication

### Basic Authentication

Use the Pipeliner API application username and password with the service URL and space ID from Show API Access.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Service URL:** `serviceUrl` · required · The regional Pipeliner service URL shown in API Access, for example https://us-east.api.pipelinersales.com.
- **Space ID:** `spaceId` · required · The Pipeliner space ID shown in API Access. This is appended to every REST API request path.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.pipelinersales.com/api-docs/overview/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `page_info.end_cursor`.

## Pagination

Use `first` in the query string to set the page size (default 30; accepted range 1–100). Use `after` in the query string as the pagination cursor.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order-by` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Upsert Products](actions/batch-upsert-products.md) | `POST /entities/Products/batch-modify` | [docs](https://pipelinercrm.eu.apidog.com/products-batch-create-or-update-3641557e0) |
| [Create Account](actions/create-account.md) | `POST /entities/Accounts` | [docs](https://pipelinercrm.eu.apidog.com/accounts-create-3640461e0) |
| [Create Contact](actions/create-contact.md) | `POST /entities/Contacts` | [docs](https://pipelinercrm.eu.apidog.com/contacts-create-3640866e0) |
| [Create Lead](actions/create-lead.md) | `POST /entities/Leads` | [docs](https://pipelinercrm.eu.apidog.com/leads-create-3641239e0) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /entities/Opportunities` | [docs](https://pipelinercrm.eu.apidog.com/opportunities-create-3641331e0) |
| [Create Product](actions/create-product.md) | `POST /entities/Products` | [docs](https://pipelinercrm.eu.apidog.com/products-create-3641555e0) |
| [Delete Account](actions/delete-account.md) | `DELETE /entities/Accounts/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/accounts-delete-3640458e0) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /entities/Contacts/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/contacts-delete-3640863e0) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /entities/Leads/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/leads-delete-3641236e0) |
| [Delete Opportunity](actions/delete-opportunity.md) | `DELETE /entities/Opportunities/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/opportunities-delete-3641328e0) |
| [Delete Product](actions/delete-product.md) | `DELETE /entities/Products/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/products-delete-3641552e0) |
| [Get Account](actions/get-account.md) | `GET /entities/Accounts/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/accounts-get-3640457e0) |
| [Get Activity](actions/get-activity.md) | `GET /entities/Activities/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/activities-get-3640556e0) |
| [Get Contact](actions/get-contact.md) | `GET /entities/Contacts/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/contacts-get-3640862e0) |
| [Get Lead](actions/get-lead.md) | `GET /entities/Leads/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/leads-get-3641235e0) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /entities/Opportunities/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/opportunities-get-3641327e0) |
| [Get Product](actions/get-product.md) | `GET /entities/Products/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/products-get-3641551e0) |
| [List Accounts](actions/list-accounts.md) | `GET /entities/Accounts` | [docs](https://pipelinercrm.eu.apidog.com/accounts-list-3640460e0) |
| [List Activities](actions/list-activities.md) | `GET /entities/Activities` | [docs](https://pipelinercrm.eu.apidog.com/activities-list-3640557e0) |
| [List Contacts](actions/list-contacts.md) | `GET /entities/Contacts` | [docs](https://pipelinercrm.eu.apidog.com/contacts-list-3640865e0) |
| [List Leads](actions/list-leads.md) | `GET /entities/Leads` | [docs](https://pipelinercrm.eu.apidog.com/leads-list-3641238e0) |
| [List Opportunities](actions/list-opportunities.md) | `GET /entities/Opportunities` | [docs](https://pipelinercrm.eu.apidog.com/opportunities-list-3641330e0) |
| [List Products](actions/list-products.md) | `GET /entities/Products` | [docs](https://pipelinercrm.eu.apidog.com/products-list-3641554e0) |
| [Merge Accounts](actions/merge-accounts.md) | `POST /entities/Accounts/merge` | [docs](https://pipelinercrm.eu.apidog.com/accounts-merge-3640462e0) |
| [Merge Contacts](actions/merge-contacts.md) | `POST /entities/Contacts/merge` | [docs](https://pipelinercrm.eu.apidog.com/contacts-merge-3640867e0) |
| [Update Account](actions/update-account.md) | `PATCH /entities/Accounts/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/accounts-update-3640459e0) |
| [Update Contact](actions/update-contact.md) | `PATCH /entities/Contacts/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/contacts-update-3640864e0) |
| [Update Lead](actions/update-lead.md) | `PATCH /entities/Leads/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/leads-update-3641237e0) |
| [Update Opportunity](actions/update-opportunity.md) | `PATCH /entities/Opportunities/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/opportunities-update-3641329e0) |
| [Update Product](actions/update-product.md) | `PATCH /entities/Products/{{id}}` | [docs](https://pipelinercrm.eu.apidog.com/products-update-3641553e0) |
