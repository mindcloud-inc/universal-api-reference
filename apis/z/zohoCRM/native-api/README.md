# Zoho CRM: Native API Reference

A consolidated summary of Zoho CRM's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/crm/developer/docs/api/v8/
- **API base URL:** `{api_domain}/crm/v8`

## Authentication

### OAuth2

OAuth2 authentication for Zoho CRM APIs

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoCRM.modules.ALL,ZohoCRM.settings.ALL,ZohoCRM.users.ALL,ZohoCRM.org.ALL,ZohoCRM.bulk.ALL,ZohoCRM.notifications.READ,ZohoCRM.notifications.CREATE,ZohoCRM.notifications.UPDATE,ZohoCRM.notifications.DELETE,ZohoCRM.coql.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/crm/developer/docs/api/v8/oauth-overview.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 200; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Lead](actions/convert-lead.md) | `POST /Leads/:record_id/actions/convert` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/convert-lead.html) |
| [Create Account](actions/create-account.md) | `POST /Accounts` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html) |
| [Create Contact](actions/create-contact.md) | `POST /Contacts` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html) |
| [Create Deal](actions/create-deal.md) | `POST /Deals` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html) |
| [Create Lead](actions/create-lead.md) | `POST /Leads` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html) |
| [Create Note for Record](actions/create-note-for-record.md) | `POST /Notes` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/create-notes.html) |
| [Create Opportunity Group](actions/create-opportunity-group.md) | `POST /Opportunity_Groups` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html) |
| [Get Account](actions/get-account.md) | `GET /Accounts` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html) |
| [Get Contact](actions/get-contact.md) | `GET /Contacts` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html) |
| [Get Deal](actions/get-deal.md) | `GET /Deals` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html) |
| [Get Fields Metadata](actions/get-fields-metadata.md) | `GET /settings/fields` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/field-meta.html) |
| [Get Lead](actions/get-lead.md) | `GET /Leads` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html) |
| [Get Modules](actions/get-modules.md) | `GET /settings/modules` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/modules-api.html) |
| [Get Notes for Record](actions/get-notes-for-record.md) | `GET /:module_api_name/:record_id/Notes` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-notes.html) |
| [Get Opportunity Group](actions/get-opportunity-group.md) | `GET /Opportunity_Groups/:opportunityGroupId` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html) |
| [Get Organization Details](actions/get-organization-details.md) | `GET /org` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-org-data.html) |
| [Get Records through COQL Query](actions/get-records-through-coql-query.md) | `POST /coql` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/Get-Records-through-COQL-Query.html) |
| [Get Related Records](actions/get-related-records.md) | `GET /:module_api_name/:record_id/:related_list_api_name` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-related-records.html) |
| [Get Users](actions/get-users.md) | `GET /users` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-users.html) |
| [List Accounts](actions/list-accounts.md) | `GET /Accounts` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html) |
| [List Contacts](actions/list-contacts.md) | `GET /Contacts` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html) |
| [List Deals](actions/list-deals.md) | `GET /Deals` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html) |
| [List Leads](actions/list-leads.md) | `GET /Leads` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html) |
| [Search Accounts](actions/search-accounts.md) | `GET /Accounts/search` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/search-records.html) |
| [Search Contacts](actions/search-contacts.md) | `GET /Contacts/search` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/search-records.html) |
| [Search Deals](actions/search-deals.md) | `GET /Deals/search` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/search-records.html) |
| [Search Leads](actions/search-leads.md) | `GET /Leads/search` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/search-records.html) |
| [Search Opportunity Groups](actions/search-opportunity-groups.md) | `GET /Opportunity_Groups/search` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/search-records.html) |
| [Update Account](actions/update-account.md) | `PUT /Accounts` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html) |
| [Update Contact](actions/update-contact.md) | `PUT /Contacts` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html) |
| [Update Deal](actions/update-deal.md) | `PUT /Deals` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html) |
| [Update Lead](actions/update-lead.md) | `PUT /Leads` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html) |
| [Update Note](actions/update-note.md) | `PUT /Notes/:note_id` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/update-notes.html) |
| [Update Opportunity Group](actions/update-opportunity-group.md) | `PUT /Opportunity_Groups` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html) |
| [Upsert Account](actions/upsert-account.md) | `POST /Accounts/upsert` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html) |
| [Upsert Contact](actions/upsert-contact.md) | `POST /Contacts/upsert` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html) |
| [Upsert Deal](actions/upsert-deal.md) | `POST /Deals/upsert` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html) |
| [Upsert Lead](actions/upsert-lead.md) | `POST /Leads/upsert` | [docs](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html) |
