# Toast: Native API Reference

A consolidated summary of Toast's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://doc.toasttab.com/openapi/
- **Orders base URL:** `{connection}`
- **Labor base URL:** `{connection}`
- **Configuration base URL:** `{connection}`

## Authentication

### OAuth 2.0 Client Credentials

Authenticate to Toast with machine-to-machine client credentials and a restaurant-specific API context.

### Credentials

- **API Hostname:** `connection` · required · The production API hostname supplied by Toast, including https:// and without a trailing slash.
- **Restaurant GUID:** `restaurantGuid` · required · The Toast GUID for the restaurant represented by this connection.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to {{credentials.connection}}/authentication/v1/authentication/login.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `restaurants:read menus:read orders:read labor:read labor.employees:read config:read`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://doc.toasttab.com/doc/devguide/authentication.html)

## API conventions

### Orders

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

### Labor

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

### Configuration

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

- **Orders:** Use `pageSize` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.
- **Configuration:** Use `pageToken` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Get Dining Option](actions/get-dining-option.md) | Configuration | `GET /config/v2/diningOptions/:guid` | [docs](https://doc.toasttab.com/openapi/configuration/operation/diningOptionsGuidGet/) |
| [Get Discount](actions/get-discount.md) | Configuration | `GET /config/v2/discounts/:guid` | [docs](https://doc.toasttab.com/openapi/configuration/operation/discountsGuidGet/) |
| [Get Employee](actions/get-employee.md) | Labor | `GET /labor/v1/employees/:employeeId` | [docs](https://doc.toasttab.com/openapi/labor/operation/employeesEmployeeIdGet/) |
| [Get Job](actions/get-job.md) | Labor | `GET /labor/v1/jobs/:jobId` | [docs](https://doc.toasttab.com/openapi/labor/operation/jobsJobIdGet/) |
| [Get Menu Item](actions/get-menu-item.md) | Configuration | `GET /config/v2/menuItems/:guid` | [docs](https://doc.toasttab.com/openapi/configuration/operation/menuItemsGuidGet/) |
| [Get Menu Metadata](actions/get-menu-metadata.md) | Menus V2 | `GET /menus/v2/metadata` | [docs](https://doc.toasttab.com/openapi/menus/operation/metadataGet/) |
| [Get Menus](actions/get-menus.md) | Menus V2 | `GET /menus/v2/menus` | [docs](https://doc.toasttab.com/openapi/menus/operation/menusGet/) |
| [Get Order](actions/get-order.md) | Orders | `GET /orders/v2/orders/:guid` | [docs](https://doc.toasttab.com/openapi/orders/operation/ordersGuidGet/) |
| [Get Restaurant](actions/get-restaurant.md) | Restaurants | `GET /restaurants/v1/restaurants/{{credentials.restaurantGuid}}` | [docs](https://doc.toasttab.com/openapi/restaurants/operation/restaurantsRestaurantGuidGet/) |
| [Get Shift](actions/get-shift.md) | Labor | `GET /labor/v1/shifts/:shiftId` | [docs](https://doc.toasttab.com/openapi/labor/operation/shiftsShiftIdGet/) |
| [Get Time Entry](actions/get-time-entry.md) | Labor | `GET /labor/v1/timeEntries/:timeEntryId` | [docs](https://doc.toasttab.com/openapi/labor/operation/timeEntriesTimeEntryIdGet/) |
| [List Dining Options](actions/list-dining-options.md) | Configuration | `GET /config/v2/diningOptions` | [docs](https://doc.toasttab.com/openapi/configuration/operation/diningOptionsGet/) |
| [List Discounts](actions/list-discounts.md) | Configuration | `GET /config/v2/discounts` | [docs](https://doc.toasttab.com/openapi/configuration/operation/discountsGet/) |
| [List Employees](actions/list-employees.md) | Labor | `GET /labor/v1/employees` | [docs](https://doc.toasttab.com/openapi/labor/operation/employeesGet/) |
| [List Jobs](actions/list-jobs.md) | Labor | `GET /labor/v1/jobs` | [docs](https://doc.toasttab.com/openapi/labor/operation/jobsGet/) |
| [List Menu Items](actions/list-menu-items.md) | Configuration | `GET /config/v2/menuItems` | [docs](https://doc.toasttab.com/openapi/configuration/operation/menuItemsGet/) |
| [List Orders](actions/list-orders.md) | Orders | `GET /orders/v2/ordersBulk` | [docs](https://doc.toasttab.com/openapi/orders/operation/ordersBulkGet/) |
| [List Revenue Centers](actions/list-revenue-centers.md) | Configuration | `GET /config/v2/revenueCenters` | [docs](https://doc.toasttab.com/openapi/configuration/operation/revenueCentersGet/) |
| [List Sales Categories](actions/list-sales-categories.md) | Configuration | `GET /config/v2/salesCategories` | [docs](https://doc.toasttab.com/openapi/configuration/operation/salesCategoriesGet/) |
| [List Service Areas](actions/list-service-areas.md) | Configuration | `GET /config/v2/serviceAreas` | [docs](https://doc.toasttab.com/openapi/configuration/operation/serviceAreasGet/) |
| [List Service Charges](actions/list-service-charges.md) | Configuration | `GET /config/v2/serviceCharges` | [docs](https://doc.toasttab.com/openapi/configuration/operation/serviceChargesGet/) |
| [List Shifts](actions/list-shifts.md) | Labor | `GET /labor/v1/shifts` | [docs](https://doc.toasttab.com/openapi/labor/operation/shiftsGet/) |
| [List Tax Rates](actions/list-tax-rates.md) | Configuration | `GET /config/v2/taxRates` | [docs](https://doc.toasttab.com/openapi/configuration/operation/taxRatesGet/) |
| [List Time Entries](actions/list-time-entries.md) | Labor | `GET /labor/v1/timeEntries` | [docs](https://doc.toasttab.com/openapi/labor/operation/timeEntriesGet/) |
