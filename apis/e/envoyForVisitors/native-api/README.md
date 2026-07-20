# Envoy for Visitors: Native API Reference

A consolidated summary of Envoy for Visitors's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.envoy.com/hub/reference
- **API base URL:** `https://api.envoy.com/v1`

## Authentication

### API Key

Use Envoy Client API Key for sandbox and private access to Envoy v1 endpoints.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://developers.envoy.com/hub/docs/getting-an-access-and-refresh)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check In Invite](actions/check-in-invite.md) | `POST /invites/:id/checkin` | [docs](https://developers.envoy.com/hub/reference/checkininvite) |
| [Check In Work Schedule](actions/check-in-work-schedule.md) | `POST /work-schedules/:id/checkin` | [docs](https://developers.envoy.com/hub/reference/checkinworkschedule) |
| [Check Out Work Schedule](actions/check-out-work-schedule.md) | `POST /work-schedules/:id/checkout` | [docs](https://developers.envoy.com/hub/reference/checkoutworkschedule) |
| [Create Entry](actions/create-entry.md) | `POST /entries` | [docs](https://developers.envoy.com/hub/reference/createentry) |
| [Create Invite](actions/create-invite.md) | `POST /invites` | [docs](https://developers.envoy.com/hub/reference/createinvite) |
| [Create Recurring Invite](actions/create-recurring-invite.md) | `POST /recurring-invites` | [docs](https://developers.envoy.com/hub/reference/createrecurringinvite) |
| [Create Work Schedule](actions/create-work-schedule.md) | `POST /work-schedules` | [docs](https://developers.envoy.com/hub/reference/createworkschedule) |
| [Delete Invite](actions/delete-invite.md) | `DELETE /invites/:id` | [docs](https://developers.envoy.com/hub/reference/deleteinvite) |
| [Get Company](actions/get-company.md) | `GET /companies` | [docs](https://developers.envoy.com/hub/reference/companies-1) |
| [Get Employee](actions/get-employee.md) | `GET /employees/:id` | [docs](https://developers.envoy.com/hub/reference/employee) |
| [Get Entry](actions/get-entry.md) | `GET /entries/:id` | [docs](https://developers.envoy.com/hub/reference/entry) |
| [Get Flow](actions/get-flow.md) | `GET /flows/:id` | [docs](https://developers.envoy.com/hub/reference/flow) |
| [Get Invite](actions/get-invite.md) | `GET /invites/:id` | [docs](https://developers.envoy.com/hub/reference/invite) |
| [Get Location](actions/get-location.md) | `GET /locations/:id` | [docs](https://developers.envoy.com/hub/reference/location) |
| [Get Recurring Invite](actions/get-recurring-invite.md) | `GET /recurring-invites/:id` | [docs](https://developers.envoy.com/hub/reference/recurringinvite) |
| [List Employees](actions/list-employees.md) | `GET /employees` | [docs](https://developers.envoy.com/hub/reference/employees-2) |
| [List Entries](actions/list-entries.md) | `GET /entries` | [docs](https://developers.envoy.com/hub/reference/entries-2) |
| [List Flows](actions/list-flows.md) | `GET /flows` | [docs](https://developers.envoy.com/hub/reference/flows-2) |
| [List Invites](actions/list-invites.md) | `GET /invites` | [docs](https://developers.envoy.com/hub/reference/invites-2) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://developers.envoy.com/hub/reference/locations-1) |
| [List Work Schedules](actions/list-work-schedules.md) | `GET /work-schedules` | [docs](https://developers.envoy.com/hub/reference/workschedules-1) |
| [Update Entry](actions/update-entry.md) | `POST /entries/:id` | [docs](https://developers.envoy.com/hub/reference/updateentry) |
| [Update Invite](actions/update-invite.md) | `POST /invites/:id` | [docs](https://developers.envoy.com/hub/reference/updateinvite) |
| [Update Recurring Invite](actions/update-recurring-invite.md) | `POST /recurring-invites/:id` | [docs](https://developers.envoy.com/hub/reference/updaterecurringinvite) |
