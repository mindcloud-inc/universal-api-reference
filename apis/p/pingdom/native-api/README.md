# Pingdom: Native API Reference

A consolidated summary of Pingdom's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.pingdom.com/api/
- **OpenAPI specification:** https://docs.pingdom.com/API_3.1.yaml
- **API base URL:** `https://api.pingdom.com/api/3.1`

## Authentication

### API Token

Use a Pingdom API token with Bearer authorization.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pingdom.com/api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `credits`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Check](actions/create-check.md) | `POST /checks` | [docs](https://docs.pingdom.com/api/#tag/Checks) |
| [Create Contact](actions/create-contact.md) | `POST /alerting/contacts` | [docs](https://docs.pingdom.com/api/#tag/Contacts) |
| [Create Maintenance Window](actions/create-maintenance-window.md) | `POST /maintenance` | [docs](https://docs.pingdom.com/api/#tag/Maintenance) |
| [Create Team](actions/create-team.md) | `POST /alerting/teams` | [docs](https://docs.pingdom.com/api/#tag/Teams) |
| [Delete Check](actions/delete-check.md) | `DELETE /checks/:checkid` | [docs](https://docs.pingdom.com/api/#tag/Checks) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /alerting/contacts/:contactid` | [docs](https://docs.pingdom.com/api/#tag/Contacts) |
| [Delete Maintenance Window](actions/delete-maintenance-window.md) | `DELETE /maintenance/:id` | [docs](https://docs.pingdom.com/api/#tag/Maintenance) |
| [Delete Team](actions/delete-team.md) | `DELETE /alerting/teams/:teamid` | [docs](https://docs.pingdom.com/api/#tag/Teams) |
| [Get Check](actions/get-check.md) | `GET /checks/:checkid` | [docs](https://docs.pingdom.com/api/#tag/Checks) |
| [Get Contact](actions/get-contact.md) | `GET /alerting/contacts/:contactid` | [docs](https://docs.pingdom.com/api/#tag/Contacts) |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://docs.pingdom.com/api/#tag/Credits) |
| [Get Maintenance Window](actions/get-maintenance-window.md) | `GET /maintenance/:id` | [docs](https://docs.pingdom.com/api/#tag/Maintenance) |
| [Get Team](actions/get-team.md) | `GET /alerting/teams/:teamid` | [docs](https://docs.pingdom.com/api/#tag/Teams) |
| [List Actions](actions/list-actions.md) | `GET /actions` | [docs](https://docs.pingdom.com/api/#tag/Actions) |
| [List Check Results](actions/list-check-results.md) | `GET /results/:checkid` | [docs](https://docs.pingdom.com/api/#tag/Results) |
| [List Checks](actions/list-checks.md) | `GET /checks` | [docs](https://docs.pingdom.com/api/#tag/Checks) |
| [List Contacts](actions/list-contacts.md) | `GET /alerting/contacts` | [docs](https://docs.pingdom.com/api/#tag/Contacts) |
| [List Maintenance Windows](actions/list-maintenance-windows.md) | `GET /maintenance` | [docs](https://docs.pingdom.com/api/#tag/Maintenance) |
| [List Teams](actions/list-teams.md) | `GET /alerting/teams` | [docs](https://docs.pingdom.com/api/#tag/Teams) |
| [Update Check](actions/update-check.md) | `PUT /checks/:checkid` | [docs](https://docs.pingdom.com/api/#tag/Checks) |
| [Update Checks](actions/update-checks.md) | `PUT /checks` | [docs](https://docs.pingdom.com/api/#tag/Checks) |
| [Update Contact](actions/update-contact.md) | `PUT /alerting/contacts/:contactid` | [docs](https://docs.pingdom.com/api/#tag/Contacts) |
| [Update Maintenance Window](actions/update-maintenance-window.md) | `PUT /maintenance/:id` | [docs](https://docs.pingdom.com/api/#tag/Maintenance) |
| [Update Team](actions/update-team.md) | `PUT /alerting/teams/:teamid` | [docs](https://docs.pingdom.com/api/#tag/Teams) |
