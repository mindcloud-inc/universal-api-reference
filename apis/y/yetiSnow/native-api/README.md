# Yeti Snow: Native API Reference

A consolidated summary of Yeti Snow's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/5759255/Uyxohiig
- **API base URL:** `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`

## Authentication

### API Key

Connect with a Yeti company token generated from Settings > API TOKENS.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.yetisoftware.com/yeti-public-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Billing Record](actions/get-billing-record.md) | `GET report/billing/show` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Contractor](actions/get-contractor.md) | `GET contractor/show/{{contractor_id}}` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Employee Timesheet](actions/get-employee-timesheet.md) | `GET report/employee_timesheet/show` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Route](actions/get-route.md) | `GET route/show` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Service](actions/get-service.md) | `GET service/show` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Site](actions/get-site.md) | `GET site/show` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Site Dataprovider](actions/get-site-dataprovider.md) | `GET site/dataprovider` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Site History](actions/get-site-history.md) | `GET history/site/show` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Site Image](actions/get-site-image.md) | `GET site_image/show` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Sub-contractor](actions/get-sub-contractor.md) | `GET sub_contractor/show/{{sub_contractor_id}}` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get Sub-contractor Billing](actions/get-sub-contractor-billing.md) | `GET report/sub_contractor/show` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get User](actions/get-user.md) | `GET user/show` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get User Filter Dataprovider](actions/get-user-filter-dataprovider.md) | `GET user/filter_dataprovider` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Get User Store Dataprovider](actions/get-user-store-dataprovider.md) | `GET user/store_dataprovider` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Billings](actions/list-billings.md) | `GET report/billing/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Contractor Sites](actions/list-contractor-sites.md) | `GET contractor/show/{{contractor_id}}/sites` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Contractor Users](actions/list-contractor-users.md) | `GET contractor/show/{{contractor_id}}/users` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Contractors](actions/list-contractors.md) | `GET contractor/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Employee Timesheets](actions/list-employee-timesheets.md) | `GET report/employee_timesheet/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Routes](actions/list-routes.md) | `GET route/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Services](actions/list-services.md) | `GET service/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Site History](actions/list-site-history.md) | `GET history/site/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Sites](actions/list-sites.md) | `GET site/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Sub-contractor Billings](actions/list-sub-contractor-billings.md) | `GET report/sub_contractor/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Sub-contractor Sites](actions/list-sub-contractor-sites.md) | `GET sub_contractor/show/{{sub_contractor_id}}/sites` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Sub-contractor Users](actions/list-sub-contractor-users.md) | `GET sub_contractor/show/{{sub_contractor_id}}/users` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Sub-contractors](actions/list-sub-contractors.md) | `GET sub_contractor/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [List Users](actions/list-users.md) | `GET user/index` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Search Contractor Companies](actions/search-contractor-companies.md) | `GET contractor/search_companies` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
| [Search Sub-contractor Companies](actions/search-sub-contractor-companies.md) | `GET sub_contractor/search_companies` | [docs](https://documenter.getpostman.com/view/5759255/Uyxohiig) |
