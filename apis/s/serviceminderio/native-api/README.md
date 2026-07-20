# serviceminder.io: Native API Reference

A consolidated summary of serviceminder.io's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://serviceminder.io/api
- **API base URL:** `https://serviceminder.com/api`

## Authentication

### API Key

Use a ServiceMinder API key generated in Control Panel > API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://serviceminder.knowledgeowl.com/help/open-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Data Subscriber Events](actions/fetch-data-subscriber-events.md) | `POST /datasubscriber/fetch` | [docs](https://serviceminder.io/api) |
| [Find Appointment](actions/find-appointment.md) | `POST /appointments/find` | [docs](https://serviceminder.io/api) |
| [Find Blogs](actions/find-blogs.md) | `POST /blogs/find` | [docs](https://serviceminder.io/api) |
| [Get Blog](actions/get-blog.md) | `POST /blogs/get` | [docs](https://serviceminder.io/api) |
| [Get Data Subscriber Download](actions/get-data-subscriber-download.md) | `POST /datasubscriber/getdownload` | [docs](https://serviceminder.io/api) |
| [Get Data Subscriber Forecasts](actions/get-data-subscriber-forecasts.md) | `POST /datasubscriber/forecasts` | [docs](https://serviceminder.io/api) |
| [Get Download](actions/get-download.md) | `POST /download/getdownload` | [docs](https://serviceminder.io/api) |
| [Get Invoice](actions/get-invoice.md) | `POST /invoice/get` | [docs](https://serviceminder.io/api) |
| [Get Organization Details](actions/get-organization-details.md) | `POST /organizations/details` | [docs](https://serviceminder.io/api) |
| [Get Part Details](actions/get-part-details.md) | `POST /part/details` | [docs](https://serviceminder.io/api) |
| [Get Part Dimensions](actions/get-part-dimensions.md) | `POST /part/getpartdimensions` | [docs](https://serviceminder.io/api) |
| [Get Proposal Details](actions/get-proposal-details.md) | `POST /proposal/details` | [docs](https://serviceminder.io/api) |
| [Get Service Details](actions/get-service-details.md) | `POST /services/details` | [docs](https://serviceminder.io/api) |
| [List Cancel Reasons](actions/list-cancel-reasons.md) | `POST /cancelreasons/all` | [docs](https://serviceminder.io/api) |
| [List Channel Campaigns](actions/list-channel-campaigns.md) | `POST /channels/campaigns` | [docs](https://serviceminder.io/api) |
| [List Channels](actions/list-channels.md) | `POST /channels/all` | [docs](https://serviceminder.io/api) |
| [List Contact Tags](actions/list-contact-tags.md) | `POST /contacts/listtags` | [docs](https://serviceminder.io/api) |
| [List Custom Fields](actions/list-custom-fields.md) | `POST /customfields/all` | [docs](https://serviceminder.io/api) |
| [List Features](actions/list-features.md) | `POST /settings/features` | [docs](https://serviceminder.io/api) |
| [List Lead Source Categories](actions/list-lead-source-categories.md) | `POST /settings/leadsourcecategories` | [docs](https://serviceminder.io/api) |
| [List Named Tax Rates](actions/list-named-tax-rates.md) | `POST /settings/namedtaxrates` | [docs](https://serviceminder.io/api) |
| [List Proposal Templates](actions/list-proposal-templates.md) | `POST /proposal/alltemplates` | [docs](https://serviceminder.io/api) |
| [List Radius Cities](actions/list-radius-cities.md) | `POST /settings/radiuscities` | [docs](https://serviceminder.io/api) |
| [List Radius Postal Codes](actions/list-radius-postal-codes.md) | `POST /settings/radiuspostalcodes` | [docs](https://serviceminder.io/api) |
| [List Service Agents](actions/list-service-agents.md) | `POST /serviceagents/all` | [docs](https://serviceminder.io/api) |
| [List Services](actions/list-services.md) | `POST /services/all` | [docs](https://serviceminder.io/api) |
| [List Users](actions/list-users.md) | `POST /user/all` | [docs](https://serviceminder.io/api) |
| [Query Appointments](actions/query-appointments.md) | `POST /appointments/query` | [docs](https://serviceminder.io/api) |
| [Query Invoices](actions/query-invoices.md) | `POST /invoice/query` | [docs](https://serviceminder.io/api) |
| [Query Organizations](actions/query-organizations.md) | `POST /organizations/query` | [docs](https://serviceminder.io/api) |
| [Query Payments](actions/query-payments.md) | `POST /payment/query` | [docs](https://serviceminder.io/api) |
| [Query Proposals](actions/query-proposals.md) | `POST /proposal/query` | [docs](https://serviceminder.io/api) |
| [Search Appointment Slots](actions/search-appointment-slots.md) | `POST /appointments/slotsearch` | [docs](https://serviceminder.io/api) |
| [Search Contacts](actions/search-contacts.md) | `POST /contacts/locate` | [docs](https://serviceminder.io/api) |
| [Test Echo](actions/test-echo.md) | `POST /test/echo` | [docs](https://serviceminder.io/api) |
