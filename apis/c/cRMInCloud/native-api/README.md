# CRM in Cloud: Native API Reference

A consolidated summary of CRM in Cloud's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.crmincloud.it/api/v1/Docs/Home
- **API base URL:** `https://app.crmincloud.it/api/latest`

## Authentication

### API Key

Authenticate CRM in Cloud Web API requests with the provider Web API key. The API key is sent as the `apikey` header and `Crm-ApplicationName` identifies the calling application when required by endpoints.

### Credentials

- **API Key:** `apiKey` · required
- **TeamSystem ID / application name:** `teamSystemId` · required · TeamSystem/application identifier used as the CRM in Cloud `Crm-ApplicationName` value for endpoints that require a calling application declaration.

Send these headers with each API request:

```http
apikey: <apiKey>
Crm-ApplicationName: <teamSystemId>
```

[Official authentication documentation](https://app.crmincloud.it/api/v1/Docs/en/Home#Authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 50; accepted range 1–500). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count activities](actions/count-activities.md) | `GET /Activity/Count` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Activity#/Count) |
| [Count appointments](actions/count-appointments.md) | `GET /Appointment/Count` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Appointment#/Count) |
| [Count companies](actions/count-companies.md) | `GET /Company/Count` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Company#/Count) |
| [Count contacts](actions/count-contacts.md) | `GET /Contact/Count` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Contact#/Count) |
| [Count leads](actions/count-leads.md) | `GET /Lead/Count` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Lead#/Count) |
| [Count lists](actions/count-lists.md) | `GET /List/Count` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/List#/Count) |
| [Count opportunities](actions/count-opportunities.md) | `GET /Opportunity/Count` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Opportunity#/Count) |
| [Count storage items](actions/count-storage-items.md) | `GET /Storage/Count` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Storage#/Count) |
| [Get new activity instance](actions/get-new-activity-instance.md) | `GET /Activity/GetNewInstance` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Activity#/GetNewInstance) |
| [Get new appointment instance](actions/get-new-appointment-instance.md) | `GET /Appointment/GetNewInstance` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Appointment#/GetNewInstance) |
| [Get new company instance](actions/get-new-company-instance.md) | `GET /Company/GetNewInstance` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Company#/GetNewInstance) |
| [Get new contact instance](actions/get-new-contact-instance.md) | `GET /Contact/GetNewInstance` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Contact#/GetNewInstance) |
| [Get new lead instance](actions/get-new-lead-instance.md) | `GET /Lead/GetNewInstance` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Lead#/GetNewInstance) |
| [Get new list instance](actions/get-new-list-instance.md) | `GET /List/GetNewInstance` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/List#/GetNewInstance) |
| [Get new opportunity instance](actions/get-new-opportunity-instance.md) | `GET /Opportunity/GetNewInstance` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Opportunity#/GetNewInstance) |
| [Get new storage item instance](actions/get-new-storage-item-instance.md) | `GET /Storage/GetNewInstance` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Storage#/GetNewInstance) |
| [Search activities](actions/search-activities.md) | `GET /Activity/Search` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Activity#/Search) |
| [Search appointments](actions/search-appointments.md) | `GET /Appointment/Search` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Appointment#/Search) |
| [Search companies](actions/search-companies.md) | `GET /Company/Search` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Company#/Search) |
| [Search contacts](actions/search-contacts.md) | `GET /Contact/Search` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Contact#/Search) |
| [Search leads](actions/search-leads.md) | `GET /Lead/Search` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Lead#/Search) |
| [Search lists](actions/search-lists.md) | `GET /List/Search` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/List#/Search) |
| [Search opportunities](actions/search-opportunities.md) | `GET /Opportunity/Search` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Opportunity#/Search) |
| [Search storage items](actions/search-storage-items.md) | `GET /Storage/Search` | [docs](https://app.crmincloud.it/api/v1/Docs/en/Controller/Storage#/Search) |
