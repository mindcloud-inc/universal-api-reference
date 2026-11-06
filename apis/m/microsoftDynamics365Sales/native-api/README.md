# Microsoft Dynamics 365 Sales: Native API Reference

A consolidated summary of Microsoft Dynamics 365 Sales's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/dynamics365/sales/developer/developer-guide
- **API base URL:** `{environmentUrl}/api/data/v9.2`

## Authentication

### Microsoft Entra ID

Connect to Dynamics 365 Sales using your Microsoft work or school account.

### Credentials

- **Tenant ID:** `tenantId` · required · Directory (tenant) ID from the Microsoft Entra app registration.
- **Environment URL:** `environmentUrl` · required · Dynamics 365 Sales environment URL, such as https://contoso.crm.dynamics.com. Omit the trailing slash and /api/data path.
- **Client ID:** `clientId` · required · Application (client) ID from your Microsoft Entra app registration.
- **Client Secret:** `clientSecret` · required · Secret Value from the Microsoft Entra app registration, not the Secret ID.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `{{credentials.environmentUrl}}/.default offline_access openid profile`.

PKCE is enabled with the `other` challenge method. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/authenticate-oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `$skiptoken` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429`. Wait 60000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `GET /accounts(:accountId)` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/account) |
| [Get Contact](actions/get-contact.md) | `GET /contacts(:contactId)` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/contact) |
| [Get Current User](actions/get-current-user.md) | `GET /WhoAmI` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/reference/whoami?view=dataverse-latest) |
| [Get Custom Record](actions/get-custom-record.md) | `GET /:entitySetName(:recordId)` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/retrieve-entity-using-web-api) |
| [Get Lead](actions/get-lead.md) | `GET /leads(:leadId)` | [docs](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/lead) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /opportunities(:opportunityId)` | [docs](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/opportunity) |
| [Get Table Definition](actions/get-table-definition.md) | `GET /EntityDefinitions(LogicalName=':logicalName')` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/query-metadata-web-api) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/account) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/contact) |
| [List Custom Records](actions/list-custom-records.md) | `GET /:entitySetName` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/query/overview) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/lead) |
| [List Opportunities](actions/list-opportunities.md) | `GET /opportunities` | [docs](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/opportunity) |
| [List Table Columns](actions/list-table-columns.md) | `GET /EntityDefinitions(LogicalName=':logicalName')/Attributes` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/query-metadata-web-api) |
| [List Tables](actions/list-tables.md) | `GET /EntityDefinitions` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/query-metadata-web-api) |
| [List Users](actions/list-users.md) | `GET /systemusers` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/reference/systemuser?view=dataverse-latest) |
| [Update Account](actions/update-account.md) | `PATCH /accounts(:accountId)` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/account) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts(:contactId)` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/contact) |
| [Update Custom Record](actions/update-custom-record.md) | `PATCH /:entitySetName(:recordId)` | [docs](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/update-delete-entities-using-web-api) |
| [Update Lead](actions/update-lead.md) | `PATCH /leads(:leadId)` | [docs](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/lead) |
| [Update Opportunity](actions/update-opportunity.md) | `PATCH /opportunities(:opportunityId)` | [docs](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/opportunity) |
