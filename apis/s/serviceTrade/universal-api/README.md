# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-13-at-14_1773424314737.png" alt="ServiceTrade logo" width="28" height="28"> ServiceTrade: Universal API

Field service management platform for commercial contractors. ServiceTrade manages locations, assets, appointments, jobs, service requests, quotes, invoices, users, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/serviceTrade/latest
- **Category:** Support / Field Service
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://servicetrade.com
- **Vendor API docs:** https://api.servicetrade.com/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get OAuth2 Userinfo](actions/get-oauth2-userinfo.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-oauth2-userinfo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset](actions/create-asset.md) | POST | Creates a new asset in ServiceTrade. |
| [Get Asset by ID](actions/get-asset-by-id.md) | GET | Retrieves an asset from ServiceTrade by ID. |
| [List Assets](actions/list-assets.md) | GET | Retrieves all assets from ServiceTrade. |
| [Update Asset](actions/update-asset.md) | PUT | Updates an existing asset in ServiceTrade. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company by ID](actions/get-company-by-id.md) | GET | Retrieves a company from ServiceTrade by ID. |
| [List Companies](actions/list-companies.md) | GET | Retrieves all companies from ServiceTrade. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact by ID](actions/get-contact-by-id.md) | GET | Retrieves a contact from ServiceTrade by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all contacts from ServiceTrade. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a new job in ServiceTrade. |
| [Get Job by ID](actions/get-job-by-id.md) | GET | Retrieves a job from ServiceTrade by ID. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves all jobs from ServiceTrade. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in ServiceTrade. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location by ID](actions/get-location-by-id.md) | GET | Retrieves a location from ServiceTrade by ID. |
| [List Locations](actions/list-locations.md) | GET | Retrieves all locations from ServiceTrade. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in ServiceTrade. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in ServiceTrade. |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST | Creates a new quote in ServiceTrade. |
| [Get Quote by ID](actions/get-quote-by-id.md) | GET | Retrieves a quote from ServiceTrade by ID. |
| [List Quotes](actions/list-quotes.md) | GET | Retrieves all quotes from ServiceTrade. |
| [Update Quote](actions/update-quote.md) | PUT | Updates an existing quote in ServiceTrade. |

### Service Requests

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Request](actions/create-service-request.md) | POST | Creates a new service request in ServiceTrade. |
| [Get Service Request by ID](actions/get-service-request-by-id.md) | GET | Retrieves a service request from ServiceTrade by ID. |
| [List Service Requests](actions/list-service-requests.md) | GET | Retrieves all service requests from ServiceTrade. |
| [Update Service Request](actions/update-service-request.md) | PUT | Updates an existing service request in ServiceTrade. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get OAuth2 Userinfo](actions/get-oauth2-userinfo.md) | GET |  |

