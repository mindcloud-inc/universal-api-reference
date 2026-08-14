# Simpro: Native API Reference

A consolidated summary of Simpro's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.simprogroup.com/apidoc/
- **API base URL:** `{buildUrl}/api/v1.0`

## Authentication

### OAuth2

### Credentials

- **Build URL:** `buildUrl` · required · Enter the full Simpro build URL for the account you want to connect, for example https://your-build.simprosuite.com.
- **Client ID:** `clientId` · required · Paste the Client ID Simpro shows after your administrator approves the API application for this build.
- **Client Secret:** `clientSecret` · required · Paste the Client Secret Simpro shows when the API application is first approved. Simpro only shows this value then, so copy it before leaving the page.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to {{credentials.buildUrl}}/oauth2/login to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.buildUrl}}/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.buildUrl}}/oauth2/token.

[Official authentication documentation](https://developer.simprogroup.com/apidoc/?page=3366d2ea7906f693b27d57ed9cca3acb#tag/Authorisation-code-grant-workflow)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /companies/:companyId/contacts/` | [docs](https://developer.simprogroup.com/apidoc/?page=9aa698f602b1e5694855cee73a683488) |
| [Create Customer](actions/create-customer.md) | `POST /companies/:companyId/customers/companies/` | [docs](https://developer.simprogroup.com/apidoc/?page=e6d0e1c8fc6a4fcf47869df87e04cd88) |
| [Create Job](actions/create-job.md) | `POST /companies/:companyId/jobs/` | [docs](https://developer.simprogroup.com/apidoc/#api-Jobs-post_api_v1_0_companies__companyID__jobs_) |
| [Create Quote](actions/create-quote.md) | `POST /companies/:companyId/quotes/` | [docs](https://developer.simprogroup.com/apidoc/#api-Quotes-post_api_v1_0_companies__companyID__quotes_) |
| [Create Site](actions/create-site.md) | `POST /companies/:companyId/sites/` | [docs](https://developer.simprogroup.com/apidoc/?page=3faa64303d5f5bcd043bb88f6768e603) |
| [Get Catalog Item](actions/get-catalog-item.md) | `GET /companies/:companyId/catalogs/:catalogId` | [docs](https://developer.simprogroup.com/apidoc/?page=5408c752aea14ba352fc3dad16b268d8) |
| [Get Company](actions/get-company.md) | `GET /companies/:companyId` | [docs](https://developer.simprogroup.com/apidoc/?page=edefbda3a2bdd979e42d8944b7325b79) |
| [Get Contact](actions/get-contact.md) | `GET /companies/:companyId/contacts/:contactId` | [docs](https://developer.simprogroup.com/apidoc/?page=9aa698f602b1e5694855cee73a683488) |
| [Get Current User](actions/get-current-user.md) | `GET /currentUser/` | [docs](https://developer.simprogroup.com/apidoc/?page=c4b3c86fec14298ef0fc42030c2507a8) |
| [Get Customer](actions/get-customer.md) | `GET /companies/:companyId/customers/companies/:customerId` | [docs](https://developer.simprogroup.com/apidoc/?page=e6d0e1c8fc6a4fcf47869df87e04cd88) |
| [Get Job](actions/get-job.md) | `GET /companies/:companyId/jobs/:jobId` | [docs](https://developer.simprogroup.com/apidoc/#api-Jobs-get_api_v1_0_companies__companyID__jobs__jobID_) |
| [Get Quote](actions/get-quote.md) | `GET /companies/:companyId/quotes/:quoteId` | [docs](https://developer.simprogroup.com/apidoc/#api-Quotes-get_api_v1_0_companies__companyID__quotes__quoteID_) |
| [Get Site](actions/get-site.md) | `GET /companies/:companyId/sites/:siteId` | [docs](https://developer.simprogroup.com/apidoc/#api-Sites-get_api_v1_0_companies__companyID__sites__siteID_) |
| [List Catalogs](actions/list-catalogs.md) | `GET /companies/:companyId/catalogs/` | [docs](https://developer.simprogroup.com/apidoc/?page=5408c752aea14ba352fc3dad16b268d8) |
| [List Companies](actions/list-companies.md) | `GET /companies/` | [docs](https://developer.simprogroup.com/apidoc/?page=edefbda3a2bdd979e42d8944b7325b79) |
| [List Contacts](actions/list-contacts.md) | `GET /companies/:companyId/contacts/` | [docs](https://developer.simprogroup.com/apidoc/?page=9aa698f602b1e5694855cee73a683488) |
| [List Customer Payments](actions/list-customer-payments.md) | `GET /companies/:companyId/customerPayments/` | [docs](https://developer.simprogroup.com/apidoc/?page=166bb94a7df2dd7995b3aca6254e02f0) |
| [List Customers](actions/list-customers.md) | `GET /companies/:companyId/customers/` | [docs](https://developer.simprogroup.com/apidoc/?page=e6d0e1c8fc6a4fcf47869df87e04cd88) |
| [List Inventory Items](actions/list-inventory-items.md) | `GET /companies/:companyId/sites/:siteId/inventory/` | [docs](https://developer.simprogroup.com/apidoc/?page=567bb087576e68109daf1d04361ff0d6) |
| [List Invoices](actions/list-invoices.md) | `GET /companies/:companyId/invoices/` | [docs](https://developer.simprogroup.com/apidoc/?page=fce9a6a1bd2a2050eb86d33103f46fd3) |
| [List Jobs](actions/list-jobs.md) | `GET /companies/:companyId/jobs/` | [docs](https://developer.simprogroup.com/apidoc/#api-Jobs-get_api_v1_0_companies__companyID__jobs_) |
| [List Quotes](actions/list-quotes.md) | `GET /companies/:companyId/quotes/` | [docs](https://developer.simprogroup.com/apidoc/#api-Quotes-get_api_v1_0_companies__companyID__quotes_) |
| [List Schedules](actions/list-schedules.md) | `GET /companies/:companyId/schedules/` | [docs](https://developer.simprogroup.com/apidoc/?page=ccdb7bf9d93e5652b57cabcc8c41e061) |
| [List Sites](actions/list-sites.md) | `GET /companies/:companyId/sites/` | [docs](https://developer.simprogroup.com/apidoc/?page=3faa64303d5f5bcd043bb88f6768e603) |
| [List Work Orders / Job Cards](actions/list-work-orders-job-cards.md) | `GET /companies/:companyId/jobs/:jobId/jobcards/` | [docs](https://developer.simprogroup.com/apidoc/?page=401740175cb9b4b5190e6d44cc5478bd) |
| [Update Contact](actions/update-contact.md) | `PATCH /companies/:companyId/contacts/:contactId` | [docs](https://developer.simprogroup.com/apidoc/?page=9aa698f602b1e5694855cee73a683488) |
| [Update Customer](actions/update-customer.md) | `PATCH /companies/:companyId/customers/companies/:customerId` | [docs](https://developer.simprogroup.com/apidoc/?page=e6d0e1c8fc6a4fcf47869df87e04cd88) |
| [Update Job](actions/update-job.md) | `PATCH /companies/:companyId/jobs/:jobId` | [docs](https://developer.simprogroup.com/apidoc/#api-Jobs-patch_api_v1_0_companies__companyID__jobs__jobID_) |
| [Update Quote](actions/update-quote.md) | `PATCH /companies/:companyId/quotes/:quoteId` | [docs](https://developer.simprogroup.com/apidoc/#api-Quotes-patch_api_v1_0_companies__companyID__quotes__quoteID_) |
| [Update Site](actions/update-site.md) | `PATCH /companies/:companyId/sites/:siteId` | [docs](https://developer.simprogroup.com/apidoc/#api-Sites-patch_api_v1_0_companies__companyID__sites__siteID_) |
