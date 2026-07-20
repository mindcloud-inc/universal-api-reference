# <img src="https://images.mindcloud.co/apps/icons/yeti-snow_1775164871428.png" alt="Yeti Snow logo" width="28" height="28"> Yeti Snow: Universal API

Field service software for snow removal and lawn care operations, including dispatch, scheduling, crew tracking, quoting, route optimization, site photos, and time tracking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yetiSnow/latest
- **Category:** Support / Field Service
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.yetisnow.com
- **Vendor API docs:** https://documenter.getpostman.com/view/5759255/Uyxohiig

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Site History](actions/get-site-history.md) | GET |  |
| [List Site History](actions/list-site-history.md) | GET |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Contractor Users](actions/list-contractor-users.md) | GET |  |
| [List Sub-contractor Users](actions/list-sub-contractor-users.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Image](actions/get-site-image.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Record](actions/get-billing-record.md) | GET |  |
| [Get Sub-contractor Billing](actions/get-sub-contractor-billing.md) | GET |  |
| [List Billings](actions/list-billings.md) | GET |  |
| [List Sub-contractor Billings](actions/list-sub-contractor-billings.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Contractor Sites](actions/list-contractor-sites.md) | GET |  |
| [List Sub-contractor Sites](actions/list-sub-contractor-sites.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Route](actions/get-route.md) | GET |  |
| [List Routes](actions/list-routes.md) | GET |  |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service](actions/get-service.md) | GET |  |
| [List Services](actions/list-services.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site](actions/get-site.md) | GET |  |
| [Get Site Dataprovider](actions/get-site-dataprovider.md) | GET |  |
| [List Sites](actions/list-sites.md) | GET |  |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Timesheet](actions/get-employee-timesheet.md) | GET |  |
| [List Employee Timesheets](actions/list-employee-timesheets.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [Get User Filter Dataprovider](actions/get-user-filter-dataprovider.md) | GET |  |
| [Get User Store Dataprovider](actions/get-user-store-dataprovider.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Get Contractor](actions/get-contractor.md) | GET |  |
| [Get Sub-contractor](actions/get-sub-contractor.md) | GET |  |
| [List Contractors](actions/list-contractors.md) | GET |  |
| [List Sub-contractors](actions/list-sub-contractors.md) | GET |  |
| [Search Contractor Companies](actions/search-contractor-companies.md) | GET |  |
| [Search Sub-contractor Companies](actions/search-sub-contractor-companies.md) | GET |  |

