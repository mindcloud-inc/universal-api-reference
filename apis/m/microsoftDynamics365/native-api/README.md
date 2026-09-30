# Microsoft Dynamics 365: Native API Reference

A consolidated summary of Microsoft Dynamics 365's API configuration and 36 documented operations.

- **API base URL:** `{baseURL}`

## Authentication

### OAuth 2.0

### Credentials

- **Client ID:** `clientId` · optional
- **Client Secret:** `MSclientSecret` · optional
- **Dynamics Instance:** `dynamicsInstance` · optional
- **Tenant ID:** `tenantId` · optional
- **Base URL:** `baseURL` · optional

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `{{credentials.dynamicsInstance}}/.default offline_access`.

Refresh expired access tokens with a POST request to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/token.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (36 documented)

| Operation | Method & path |
| --- | --- |
| [Create Account](actions/create-account.md) | `POST /accounts` |
| [Create Contact](actions/create-contact.md) | `POST /contacts` |
| [Create Custom Entity](actions/create-custom-entity.md) | `POST :tableName` |
| [Create Customer](actions/create-customer.md) | `POST Customers` |
| [Create Customer Postal Address](actions/create-customer-postal-address.md) | `POST CustomerPostalAddresses` |
| [Create Distinct Product](actions/create-distinct-product.md) | `POST DistinctProducts` |
| [Create ProductsV2 Entity](actions/create-products-v2-entity.md) | `POST ProductsV2` |
| [Create Project](actions/create-project.md) | `POST Projects` |
| [Create Project Contract](actions/create-project-contract.md) | `POST ProjectContracts` |
| [Create Project Sales Item Requirement](actions/create-project-sales-item-requirement.md) | `POST ProjectSalesItemRequirements` |
| [Create Sellable Released Product](actions/create-sellable-released-product.md) | `POST SellableReleasedProducts` |
| [Create WBS Activity Estimate](actions/create-wbs-activity-estimate.md) | `POST ProjWBSActivityEstimates` |
| [Create WBS Draft Entity](actions/create-wbs-draft-entity.md) | `POST ProjectWBSDrafts` |
| [Get Accounts](actions/get-accounts.md) | `GET /accounts` |
| [Get All Available Entities](actions/get-all-available-entities.md) | `GET` |
| [Get Contact By Id](actions/get-contact-by-id.md) | `GET /api/data/v9.2/contacts(:contactId)` |
| [Get Contacts](actions/get-contacts.md) | `GET /contacts` |
| [Get Custom APIs](actions/get-custom-ap-is.md) | `GET /api/data/v9.2/customapis` |
| [Get Custom Table](actions/get-custom-table.md) | `GET :tableName` |
| [Get Custom Table Entry By Id](actions/get-custom-table-entry-by-id.md) | `GET /:tableName(:id)` |
| [Get Customers](actions/get-customers.md) | `GET Customers` |
| [Get Distinct Products](actions/get-distinct-products.md) | `GET` |
| [Get Logistics Postal Address BI Entities](actions/get-logistics-postal-address-bi-entities.md) | `GET LogisticsPostalAddressBiEntities` |
| [Get ProductsV2](actions/get-products-v2.md) | `GET ProductsV2` |
| [Get Project Contracts](actions/get-project-contracts.md) | `GET ProjectContracts` |
| [Get Projects](actions/get-projects.md) | `GET Projects` |
| [Get Released Products V2](actions/get-released-products-v2.md) | `GET ReleasedProductsV2` |
| [Get Sellable Released Products](actions/get-sellable-released-products.md) | `GET SellableReleasedProducts` |
| [Get System Users](actions/get-system-users.md) | `GET /systemusers` |
| [Get Trv Exp Mobile Activities](actions/get-trv-exp-mobile-activities.md) | `GET TrvExpMobileActivities` |
| [Get Workers](actions/get-workers.md) | `GET /Workers` |
| [Patch Accounts](actions/patch-accounts.md) | `PATCH /accounts(:accountsId)` |
| [Patch Contact](actions/patch-contact.md) | `PATCH /contacts(:contactId)` |
| [Patch Custom Table](actions/patch-custom-table.md) | `PATCH :tableName(:filter)` |
| [Patch Custom Table Field](actions/patch-custom-table-field.md) | `PATCH /:tableName(:id)` |
| [Search Entity Definition](actions/search-entity-definition.md) | `GET /EntityDefinitions(LogicalName=':logicalName')` |
