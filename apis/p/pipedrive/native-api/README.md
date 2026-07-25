# Pipedrive: Native API Reference

A consolidated summary of Pipedrive's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://developers.pipedrive.com/docs/api/v1
- **API base URL:** `{api_domain}/api`

## Authentication

### OAuth 2.0

OAuth2 for Pipedrive private/public app access.

### Credentials

- **Company Domain:** `companyDomain` · required · Pipedrive company domain (e.g. mindcloud-connection.pipedrive.com).

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://oauth.pipedrive.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth.pipedrive.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `base deals:full activities:full contacts:full products:full search:read leads:full projects:full webhooks:full dealFields:full users:full organizations:full`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth.pipedrive.com/oauth/token.

[Official authentication documentation](https://pipedrive.readme.io/docs/marketplace-oauth-authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `data.additional_data.next_cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–500). Use `cursor` in the query string as the pagination cursor.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Activity](actions/add-activity.md) | `POST v2/activities` | [docs](https://developers.pipedrive.com/docs/api/v1/Activities#addActivity) |
| [Add Deal](actions/add-deal.md) | `POST v2/deals` | [docs](https://developers.pipedrive.com/docs/api/v1/Deals#addDeal) |
| [Add Lead](actions/add-lead.md) | `POST v1/leads` | [docs](https://developers.pipedrive.com/docs/api/v1/Leads) |
| [Add Organization](actions/add-organization.md) | `POST v2/organizations` | [docs](https://developers.pipedrive.com/docs/api/v1/Organizations#addOrganization) |
| [Add Person](actions/add-person.md) | `POST v2/persons` | [docs](https://developers.pipedrive.com/docs/api/v1/Persons#addPerson) |
| [Add Product](actions/add-product.md) | `POST v2/products` | [docs](https://developers.pipedrive.com/docs/api/v1/Products) |
| [Add Product to Deal](actions/add-product-to-deal.md) | `POST v2/deals/:dealId/products` |  |
| [Add Webhook](actions/add-webhook.md) | `POST v1/webhooks` | [docs](https://developers.pipedrive.com/docs/api/v1/Webhooks#addWebhook) |
| [Convert Deal To Lead](actions/convert-deal-to-lead.md) | `POST v2/deals/:id/convert/lead` | [docs](https://developers.pipedrive.com/docs/api/v1/Deals#convertDealToLead) |
| [Convert Lead To Deal](actions/convert-lead-to-deal.md) | `POST v2/leads/:id/convert/deal` | [docs](https://developers.pipedrive.com/docs/api/v1/Leads) |
| [Delete Activity](actions/delete-activity.md) | `DELETE v2/activities/:id` | [docs](https://developers.pipedrive.com/docs/api/v1/Activities#deleteActivity) |
| [Delete Deal](actions/delete-deal.md) | `DELETE v2/deals/:id` | [docs](https://developers.pipedrive.com/docs/api/v1/Deals#deleteDeal) |
| [Get Activities](actions/get-activities.md) | `GET v2/activities` | [docs](https://developers.pipedrive.com/docs/api/v1/Activities#getActivities) |
| [Get All Deal Fields](actions/get-all-deal-fields.md) | `GET v2/dealFields` | [docs](https://developers.pipedrive.com/docs/api/v1/DealFields#getDealFields) |
| [Get All Product Fields](actions/get-all-deal-fields-copy.md) | `GET v2/productFields` | [docs](https://developers.pipedrive.com/docs/api/v1/DealFields#getDealFields) |
| [Get Deal](actions/get-deal.md) | `GET v2/deals/:id` | [docs](https://developers.pipedrive.com/docs/api/v1/Deals#getDeal) |
| [Get Deals Summary](actions/get-deals-summary.md) | `GET v1/deals/summary` | [docs](https://developers.pipedrive.com/docs/api/v1/Deals#getDealsSummary) |
| [Get Leads](actions/get-leads.md) | `GET v1/leads` | [docs](https://developers.pipedrive.com/docs/api/v1/Leads) |
| [Get Organization](actions/get-organization.md) | `GET v2/organizations/:id` | [docs](https://developers.pipedrive.com/docs/api/v1/Organizations#getOrganization) |
| [Get Organizations](actions/get-organizations.md) | `GET v2/organizations` | [docs](https://developers.pipedrive.com/docs/api/v1/Organizations#getOrganizations) |
| [Get Person](actions/get-person.md) | `GET v2/persons/:id` | [docs](https://developers.pipedrive.com/docs/api/v1/Persons#getPerson) |
| [Get Persons](actions/get-persons.md) | `GET v2/persons` | [docs](https://developers.pipedrive.com/docs/api/v1/Persons#getPersons) |
| [Get Products](actions/get-products.md) | `GET v2/products` | [docs](https://developers.pipedrive.com/docs/api/v1/Products) |
| [List Deals](actions/list-deals.md) | `GET v2/deals` | [docs](https://developers.pipedrive.com/docs/api/v1/Deals#getDealsCollection) |
| [Search Deals](actions/search-deals.md) | `GET v2/deals/search` | [docs](https://developers.pipedrive.com/docs/api/v1/Deals#searchDeals) |
| [Search Leads](actions/search-leads.md) | `GET v2/leads/search` | [docs](https://developers.pipedrive.com/docs/api/v1/Leads) |
| [Search Organizations](actions/search-organization.md) | `GET v2/organizations/search` | [docs](https://developers.pipedrive.com/docs/api/v1/Organizations#getOrganizationsSearch) |
| [Search Persons](actions/search-persons.md) | `GET v2/persons/search` | [docs](https://developers.pipedrive.com/docs/api/v1/Persons#searchPersons) |
| [Search Products](actions/search-products.md) | `GET v2/products/search` | [docs](https://developers.pipedrive.com/docs/api/v1/Products) |
| [Update a Product](actions/update-a-product.md) | `PATCH v2/products/:productId` | [docs](https://developers.pipedrive.com/docs/api/v1/Products#updateAProduct) |
| [Update Activity](actions/update-activity.md) | `PATCH v2/activities/:id` | [docs](https://developers.pipedrive.com/docs/api/v1/Activities#updateActivity) |
| [Update Deal](actions/update-deal.md) | `PATCH v2/deals/:id` | [docs](https://developers.pipedrive.com/docs/api/v1/Deals#updateDeal) |
| [Update Organization](actions/update-organization.md) | `PATCH v2/organizations/:id` | [docs](https://developers.pipedrive.com/docs/api/v1/Organizations#updateOrganization) |
| [Update Person](actions/update-person.md) | `PATCH v2/persons/:id` | [docs](https://developers.pipedrive.com/docs/api/v1/Persons#updatePerson) |
