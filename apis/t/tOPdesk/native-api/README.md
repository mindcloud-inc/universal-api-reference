# TOPdesk: Native API Reference

A consolidated summary of TOPdesk's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://developers.topdesk.com/
- **OpenAPI specification:** https://developers.topdesk.com/
- **API base URL:** `https://usatopdesktrial2.topdesk.net/tas/api/`

## Authentication

### Basic

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.topdesk.com/en/authentication-for-action-sequences.html)

## Pagination

Use `limit` in the query string to set the page size (default 25; minimum 1). Use `cursor` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Incident Time Spent](actions/add-incident-time-spent.md) | `POST /incidents/id/:id/timespent` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Archive Incident by ID](actions/archive-incident-by-id.md) | `PUT /incidents/id/:id/archive` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Create Incident](actions/create-incident.md) | `POST /incidents` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Deescalate Incident by ID](actions/deescalate-incident-by-id.md) | `PUT /incidents/id/:id/deescalate` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Escalate Incident by ID](actions/escalate-incident-by-id.md) | `PUT /incidents/id/:id/escalate` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Get Incident by ID](actions/get-incident-by-id.md) | `GET /incidents/id/:id` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Get Incident by Number](actions/get-incident-by-number.md) | `GET /incidents/number/:number` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Get Incident Progress Trail Count](actions/get-incident-progress-trail-count.md) | `GET /incidents/id/:id/progresstrail/count` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Get Incident Time Spent](actions/get-incident-time-spent.md) | `GET /incidents/id/:id/timespent` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Deescalation Reasons](actions/list-deescalation-reasons.md) | `GET /incidents/deescalation-reasons` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Escalation Reasons](actions/list-escalation-reasons.md) | `GET /incidents/escalation-reasons` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incident Actions](actions/list-incident-actions.md) | `GET /incidents/id/:id/actions` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incident Call Types](actions/list-incident-call-types.md) | `GET /incidents/call_types` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incident Categories](actions/list-incident-categories.md) | `GET /incidents/categories` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incident Priorities](actions/list-incident-priorities.md) | `GET /incidents/priorities` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incident Progress Trail](actions/list-incident-progress-trail.md) | `GET /incidents/id/:id/progresstrail` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incident Requests](actions/list-incident-requests.md) | `GET /incidents/id/:id/requests` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incident Statuses](actions/list-incident-statuses.md) | `GET /incidents/statuses` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incident Subcategories](actions/list-incident-subcategories.md) | `GET /incidents/subcategories` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incident Urgencies](actions/list-incident-urgencies.md) | `GET /incidents/urgencies` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [List Incidents](actions/list-incidents.md) | `GET /incidents` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Replace Incident by ID](actions/replace-incident-by-id.md) | `PUT /incidents/id/:id` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Replace Incident by Number](actions/replace-incident-by-number.md) | `PUT /incidents/number/:number` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Unarchive Incident by ID](actions/unarchive-incident-by-id.md) | `PUT /incidents/id/:id/unarchive` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Update Incident by ID (Patch)](actions/update-incident-by-id-patch.md) | `PATCH /incidents/id/:id` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
| [Update Incident by Number (Patch)](actions/update-incident-by-number-patch.md) | `PATCH /incidents/number/:number` | [docs](https://developers.topdesk.com/explorer/?page=incident) |
