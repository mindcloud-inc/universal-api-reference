# U-ON: Native API Reference

A consolidated summary of U-ON's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.u-on.travel/doc
- **API base URL:** `https://api.u-on.ru/{key}`

## Authentication

### API Key

U-ON.Travel API key. The key is inserted into the API URL path as documented by U-ON.Travel.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.u-on.travel/doc)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the request parameters to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Tourist by Phone](actions/find-tourist-by-phone.md) | `GET /user/phone/{phone}.json` | [docs](https://api.u-on.travel/doc) |
| [Get Bill](actions/get-bill.md) | `GET /bill/{id}.json` | [docs](https://api.u-on.travel/doc) |
| [Get Hotel](actions/get-hotel.md) | `GET /hotel/{id}.json` | [docs](https://api.u-on.travel/doc) |
| [Get Lead](actions/get-lead.md) | `GET /lead/{id}.json` | [docs](https://api.u-on.travel/doc) |
| [Get Manager](actions/get-manager.md) | `GET /manager/{user_id}.json` | [docs](https://api.u-on.travel/doc) |
| [Get Payment](actions/get-payment.md) | `GET /payment/{id}.json` | [docs](https://api.u-on.travel/doc) |
| [Get Request](actions/get-request.md) | `GET /request/{id}.json` | [docs](https://api.u-on.travel/doc) |
| [Get Supplier](actions/get-supplier.md) | `GET /supplier/{id}.json` | [docs](https://api.u-on.travel/doc) |
| [Get Tourist](actions/get-tourist.md) | `GET /user/{id}.json` | [docs](https://api.u-on.travel/doc) |
| [List Bills](actions/list-bills.md) | `GET /bills/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Cities](actions/list-cities.md) | `GET /cities/{country_id}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Closed Requests](actions/list-closed-requests.md) | `GET /requests/closed/{date_from}/{date_to}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Companies](actions/list-companies.md) | `GET /company.json` | [docs](https://api.u-on.travel/doc) |
| [List Company Offices](actions/list-company-offices.md) | `GET /company-office.json` | [docs](https://api.u-on.travel/doc) |
| [List Countries](actions/list-countries.md) | `GET /countries.json` | [docs](https://api.u-on.travel/doc) |
| [List Currencies](actions/list-currencies.md) | `GET /currency.json` | [docs](https://api.u-on.travel/doc) |
| [List Hotels](actions/list-hotels.md) | `GET /hotels/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Lead Statuses](actions/list-lead-statuses.md) | `GET /status_lead.json` | [docs](https://api.u-on.travel/doc) |
| [List Leads](actions/list-leads.md) | `GET /leads/{date_from}/{date_to}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Leads by Client](actions/list-leads-by-client.md) | `GET /lead-by-client/{id}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Managers](actions/list-managers.md) | `GET /manager.json` | [docs](https://api.u-on.travel/doc) |
| [List Managers by Office](actions/list-managers-by-office.md) | `GET /manager/office/{office_id}.json` | [docs](https://api.u-on.travel/doc) |
| [List Payment Statuses](actions/list-payment-statuses.md) | `GET /status_pay.json` | [docs](https://api.u-on.travel/doc) |
| [List Payments](actions/list-payments.md) | `GET /payment/list/{date_from}/{date_to}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Request Statuses](actions/list-request-statuses.md) | `GET /status.json` | [docs](https://api.u-on.travel/doc) |
| [List Requests](actions/list-requests.md) | `GET /requests/{date_from}/{date_to}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Requests by Client](actions/list-requests-by-client.md) | `GET /request-by-client/{id}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Requests by Tourist](actions/list-requests-by-tourist.md) | `GET /request-by-tourist/{id}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Service Types](actions/list-service-types.md) | `GET /service_type.json` | [docs](https://api.u-on.travel/doc) |
| [List Sources](actions/list-sources.md) | `GET /source.json` | [docs](https://api.u-on.travel/doc) |
| [List Suppliers](actions/list-suppliers.md) | `GET /suppliers/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Tourists](actions/list-tourists.md) | `GET /users/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Travel Types](actions/list-travel-types.md) | `GET /travel-type.json` | [docs](https://api.u-on.travel/doc) |
| [List Updated Leads](actions/list-updated-leads.md) | `GET /leads/updated/{date_from}/{date_to}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Updated Requests](actions/list-updated-requests.md) | `GET /requests/updated/{date_from}/{date_to}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [List Updated Tourists](actions/list-updated-tourists.md) | `GET /user/updated/{date_from}/{date_to}/{page}.json` | [docs](https://api.u-on.travel/doc) |
| [Search Leads](actions/search-leads.md) | `POST /lead/search.json` | [docs](https://api.u-on.travel/doc) |
| [Search Requests](actions/search-requests.md) | `POST /request/search.json` | [docs](https://api.u-on.travel/doc) |
| [Search Services](actions/search-services.md) | `POST /service/search.json` | [docs](https://api.u-on.travel/doc) |
| [Search Tourists](actions/search-tourists.md) | `POST /user/search.json` | [docs](https://api.u-on.travel/doc) |
