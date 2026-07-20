# SIGNL4: Native API Reference

A consolidated summary of SIGNL4's API configuration and 47 documented operations, with links to official documentation.

- **Official docs:** https://docs.signl4.com/integrations/rest-api/rest-api.html
- **OpenAPI specification:** https://connect.signl4.com/api/docs/v2/swagger.json
- **API base URL:** `https://connect.signl4.com/api`

## Authentication

### API Key

Authenticate SIGNL4 requests with the API key sent in the X-S4-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://connect.signl4.com/api/docs/index.html)

## API conventions

Responses from this API use JSON.

## Endpoints (47 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Alert](actions/acknowledge-alert.md) | `POST /v2/alerts/{alertId}/acknowledge` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Add User To Team](actions/add-user-to-team.md) | `POST /v2/teams/{teamId}/memberships/{userId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Annotate Alert](actions/annotate-alert.md) | `POST /v2/alerts/{alertId}/annotate` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Close Alert](actions/close-alert.md) | `POST /v2/alerts/{alertId}/close` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Create Alert Summary](actions/create-alert-summary.md) | `POST /v2/alerts/{alertId}/summarize` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Create Category](actions/create-category.md) | `POST /v2/categories/{teamId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Create Event](actions/create-event.md) | `POST /v2/events/{webhookIdOrTeamId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Create Event Source](actions/create-event-source.md) | `POST /v2/eventsources` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Delete Category](actions/delete-category.md) | `DELETE /v2/categories/{teamId}/{categoryId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Delete Event Source](actions/delete-event-source.md) | `DELETE /v2/eventsources/{eventSourceId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Alert](actions/get-alert.md) | `GET /v2/alerts/{alertId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Alert Details](actions/get-alert-details.md) | `GET /v2/alerts/{alertId}/details` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Alert Distribution](actions/get-alert-distribution.md) | `GET /v2/alerts/{alertId}/distribution` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Alert Notifications](actions/get-alert-notifications.md) | `GET /v2/alerts/{alertId}/notifications` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Alert Parameters](actions/get-alert-parameters.md) | `GET /v2/alerts/{alertId}/parameters` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Alert Report](actions/get-alert-report.md) | `GET /v2/alerts/report` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Alert Summary](actions/get-alert-summary.md) | `GET /v2/alerts/{alertId}/summary` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Alert Timeline](actions/get-alert-timeline.md) | `GET /v2/alerts/{alertId}/timeline` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Category Metrics](actions/get-category-metrics.md) | `GET /v2/categories/{teamId}/{categoryId}/metrics` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Duty Summary](actions/get-duty-summary.md) | `GET /v2/duties/summary` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Event](actions/get-event.md) | `GET /v2/events/{eventId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Event Overview](actions/get-event-overview.md) | `GET /v2/events/{eventId}/overview` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Event Parameters](actions/get-event-parameters.md) | `GET /v2/events/{eventId}/parameters` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Event Source](actions/get-event-source.md) | `GET /v2/eventsources/{eventSourceId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Subscription](actions/get-subscription.md) | `GET /v2/subscriptions/{subscriptionId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Team](actions/get-team.md) | `GET /v2/teams/{teamId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Team Alert Settings](actions/get-team-alert-settings.md) | `GET /v2/teams/{teamId}/alertSettings` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get Team Setup Progress](actions/get-team-setup-progress.md) | `GET /v2/teams/{teamId}/setupProgress` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get User](actions/get-user.md) | `GET /v2/users/{userId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Get User Duty Status](actions/get-user-duty-status.md) | `GET /v2/users/{userId}/dutyStatus` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Alerts](actions/list-alerts.md) | `POST /v2/alerts/paged` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Event Sources](actions/list-event-sources.md) | `GET /v2/eventsources` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Events](actions/list-events.md) | `POST /v2/events/paged` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Subscription Teams](actions/list-subscription-teams.md) | `GET /v2/subscriptions/{subscriptionId}/teams` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v2/subscriptions` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Team Categories](actions/list-team-categories.md) | `GET /v2/categories/{teamId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Team Event Sources](actions/list-team-event-sources.md) | `GET /v2/teams/{teamId}/eventSources` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Team Memberships](actions/list-team-memberships.md) | `GET /v2/teams/{teamId}/memberships` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Teams](actions/list-teams.md) | `GET /v2/teams` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [List Users](actions/list-users.md) | `GET /v2/users` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Punch User In](actions/punch-user-in.md) | `POST /v2/duties/punchIn` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Punch User Out](actions/punch-user-out.md) | `POST /v2/duties/punchOut` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Remove Team Membership](actions/remove-team-membership.md) | `DELETE /v2/teams/{teamId}/memberships/{userId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Trigger Alert](actions/trigger-alert.md) | `POST /v2/alerts` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Update Category](actions/update-category.md) | `PUT /v2/categories/{teamId}/{categoryId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Update Event Source](actions/update-event-source.md) | `PUT /v2/eventsources/{eventSourceId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
| [Update Team Membership](actions/update-team-membership.md) | `PUT /v2/teams/{teamId}/memberships/{userId}` | [docs](https://connect.signl4.com/api/docs/index.html) |
