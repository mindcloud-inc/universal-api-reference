# Teamgate: Native API Reference

A consolidated summary of Teamgate's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.teamgate.com/
- **API base URL:** `https://api.teamgate.com/v4`

## Authentication

### Custom Headers

Connect with Teamgate APP_KEY and AUTH_TOKEN header credentials.

### Credentials

- **App Key:** `appKey` · required · Teamgate application key from Settings -> Additional features -> External Apps.
- **Auth Token:** `authToken` · required · Teamgate user auth token from My Profile -> Integrations -> API access.

Send these headers with each API request:

```http
X-App-Key: <appKey>
X-Auth-Token: <authToken>
```

[Official authentication documentation](https://developers.teamgate.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | `POST /events` | [docs](https://developers.teamgate.com/#a9a32135-d073-4a29-9f9a-2341531a9039) |
| [Create Call](actions/create-call.md) | `POST /events` | [docs](https://developers.teamgate.com/#54abed6f-fc8e-44f0-bd66-8f0c15186299) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://developers.teamgate.com/#2b3a0450-e365-4f89-b02c-e817d997f627) |
| [Create Deal](actions/create-deal.md) | `POST /deals` | [docs](https://developers.teamgate.com/#7cf909d7-b66c-4ddb-ac3b-bb800f8b4ae5) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://developers.teamgate.com/#8921df2b-3158-4b16-b81c-c37c6414c20f) |
| [Create Note](actions/create-note.md) | `POST /events` | [docs](https://developers.teamgate.com/#f7b1d7c0-2c20-4dfc-9e27-39b3d9f6fc59) |
| [Create Person](actions/create-person.md) | `POST /people` | [docs](https://developers.teamgate.com/#6a612101-c0cb-404c-9442-29d07c352185) |
| [Create Task](actions/create-task.md) | `POST /events` | [docs](https://developers.teamgate.com/#85dac403-ccf3-4140-9a43-35f82403cd18) |
| [Delete Company](actions/delete-company.md) | `DELETE /companies/{{companyId}}` | [docs](https://developers.teamgate.com/#46a989fe-7c13-4abc-8114-1600cc9e2d41) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /deals/:deal_id` | [docs](https://developers.teamgate.com/#30b15db5-e284-4274-9871-a6fde39fded2) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /leads/{{leadId}}` | [docs](https://developers.teamgate.com/#b0581d75-f1f5-49a2-a601-d8d28279ce87) |
| [Delete Person](actions/delete-person.md) | `DELETE /people/{{personId}}` | [docs](https://developers.teamgate.com/#6792ed0c-bdb7-41ae-b298-a205a54a6fbf) |
| [Get Activity](actions/get-activity.md) | `GET /events/{{eventId}}` | [docs](https://developers.teamgate.com/#5b576f18-5b18-4fb0-9cbf-8d02343420d5) |
| [Get Company](actions/get-company.md) | `GET /companies/{{companyId}}` | [docs](https://developers.teamgate.com/#480a8a97-aae6-4a18-b545-a69037b88ed1) |
| [Get Deal](actions/get-deal.md) | `GET /deals/:deal_id` | [docs](https://developers.teamgate.com/#b692423c-78f3-449b-bb8b-ad73a240f833) |
| [Get Lead](actions/get-lead.md) | `GET /leads/{{leadId}}` | [docs](https://developers.teamgate.com/#ae9b225d-0b86-4d15-9ec4-ddba3764c3cf) |
| [Get Person](actions/get-person.md) | `GET /people/{{personId}}` | [docs](https://developers.teamgate.com/#c9850d4a-77f9-411f-8652-b924b6160723) |
| [List Activities](actions/list-activities.md) | `GET /events` | [docs](https://developers.teamgate.com/#ada4ee7b-a006-4e7c-9dee-a1db57e36755) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://developers.teamgate.com/#cd8d915d-8ba3-4fbc-9932-7e6a3c4dcc08) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /customFields` | [docs](https://developers.teamgate.com/#d1ebf1aa-aed5-41df-a8b0-eb36c8221c0d) |
| [List Deal Companies](actions/list-deal-companies.md) | `GET /deals/:deal_id/companies` | [docs](https://developers.teamgate.com/#c6b214ac-7853-4a7f-8164-bd7bdd91c8fc) |
| [List Deal People](actions/list-deal-people.md) | `GET /deals/:deal_id/people` | [docs](https://developers.teamgate.com/#eeb59e67-b8a4-4abc-92ad-dcd72ae69d3f) |
| [List Deals](actions/list-deals.md) | `GET /deals` | [docs](https://developers.teamgate.com/#8f23eadd-e356-4b45-bdbe-b1122da6f762) |
| [List Lead Activities](actions/list-lead-activities.md) | `GET /leads/{{leadId}}/events` | [docs](https://developers.teamgate.com/#0b9f8299-f529-45c2-b768-a465b14d4084) |
| [List Lead Statuses](actions/list-lead-statuses.md) | `GET /leadsStatuses` | [docs](https://developers.teamgate.com/#a4b61894-5087-4a91-852d-927851333503) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://developers.teamgate.com/#4a60be88-9991-41d2-8949-7a0f47319c80) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://developers.teamgate.com/#7eb019a9-9168-4056-a507-75bd32c105e0) |
| [List Person Deals](actions/list-person-deals.md) | `GET /people/{{personId}}/deals` | [docs](https://developers.teamgate.com/#c6e6df8c-e097-4d8a-b060-2d2b5d08fde4) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipelines` | [docs](https://developers.teamgate.com/#43821ad0-cf31-443b-9392-4c529ab2d3a6) |
| [List Sources](actions/list-sources.md) | `GET /sources` | [docs](https://developers.teamgate.com/#1071580d-c1b8-41ef-b1b3-2c73f3bc5723) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.teamgate.com/#9f5e25bd-ad02-4d73-a912-24216c525cb9) |
| [Search Companies](actions/search-companies.md) | `GET /companies` | [docs](https://developers.teamgate.com/#5123441a-7bc1-4ab6-a79d-42e536804a91) |
| [Search Deals](actions/search-deals.md) | `GET /deals` | [docs](https://developers.teamgate.com/#bc81c42a-8448-43af-8991-4eeea7feeef1) |
| [Search Leads](actions/search-leads.md) | `GET /leads` | [docs](https://developers.teamgate.com/#1b80ca61-833a-472a-b127-e3b6d5e18902) |
| [Search People](actions/search-people.md) | `GET /people` | [docs](https://developers.teamgate.com/#7708cc10-52d4-4ec3-bcc5-1222f21480bb) |
| [Update Activity](actions/update-activity.md) | `PUT /events/{{eventId}}` | [docs](https://developers.teamgate.com/#5fecc71a-e467-4272-bed4-dc2b5b8e0341) |
| [Update Company](actions/update-company.md) | `PUT /companies/{{companyId}}` | [docs](https://developers.teamgate.com/#39f561e7-d276-49a7-8873-1fc1a6758837) |
| [Update Deal](actions/update-deal.md) | `PUT /deals/:deal_id` | [docs](https://developers.teamgate.com/#fe590427-fcb9-4689-9671-7d3daa235b1a) |
| [Update Lead](actions/update-lead.md) | `PUT /leads/{{leadId}}` | [docs](https://developers.teamgate.com/#175ab11d-d675-4c34-8fb9-638027d11ae9) |
| [Update Person](actions/update-person.md) | `PUT /people/{{personId}}` | [docs](https://developers.teamgate.com/#39163c34-52c9-440d-ba20-6067160c3812) |
