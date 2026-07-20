# Mixpanel: Native API Reference

A consolidated summary of Mixpanel's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://developer.mixpanel.com/reference/overview
- **API base URL:** `https://mixpanel.com/api`

## Authentication

### Service Account

Authenticate with a Mixpanel service account username and secret.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Region And Domain:** `regionAndDomain` · optional · Mixpanel API host token used in docs as {regionAndDomain}.com.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.mixpanel.com/reference/authentication-methods#service-account-authentication-details)

### Project Secret

Authenticate with a Mixpanel project secret using HTTP Basic auth.

### Credentials

- **API Key:** `apiKey` · required
- **Region And Domain:** `regionAndDomain` · optional · Mixpanel API host token used in docs as {regionAndDomain}.com.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.mixpanel.com/reference/authentication-methods#project-secret-authentication-details)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Append to Profile List Property](actions/append-to-profile-list-property.md) | `POST https://api.mixpanel.com/engage` | [docs](https://developer.mixpanel.com/reference/profile-append-to-list-property) |
| [Batch Update Group Profiles](actions/batch-update-group-profiles.md) | `POST https://api.mixpanel.com/groups` | [docs](https://developer.mixpanel.com/reference/group-batch-update) |
| [Create Alias](actions/create-alias.md) | `POST https://api.mixpanel.com/track` | [docs](https://developer.mixpanel.com/reference/identity-create-alias) |
| [Create Annotation](actions/create-annotation.md) | `POST /app/projects/:projectId/annotations` | [docs](https://developer.mixpanel.com/reference/create-annotation) |
| [Delete Annotation](actions/delete-annotation.md) | `DELETE /app/projects/:projectId/annotations/:annotationId` | [docs](https://developer.mixpanel.com/reference/delete-annotation-1) |
| [Delete Group Property](actions/delete-group-property.md) | `POST https://api.mixpanel.com/groups` | [docs](https://developer.mixpanel.com/reference/group-delete-property) |
| [Delete Profile Property](actions/delete-profile-property.md) | `POST https://api.mixpanel.com/engage` | [docs](https://developer.mixpanel.com/reference/profile-delete-property) |
| [Export Events](actions/export-events.md) | `GET https://data.mixpanel.com/api/2.0/export` | [docs](https://developer.mixpanel.com/reference/raw-event-export) |
| [Get Annotation](actions/get-annotation.md) | `GET /app/projects/:projectId/annotations/:annotationId` | [docs](https://developer.mixpanel.com/reference/get-annotation-1) |
| [Get Profile Event Activity](actions/get-profile-event-activity.md) | `GET /query/stream/query` | [docs](https://developer.mixpanel.com/reference/activity-stream-query) |
| [Import Events](actions/import-events.md) | `POST https://api.mixpanel.com/import` | [docs](https://developer.mixpanel.com/reference/import-events) |
| [Increment Profile Numerical Property](actions/increment-profile-numerical-property.md) | `POST https://api.mixpanel.com/engage` | [docs](https://developer.mixpanel.com/reference/profile-numerical-add) |
| [List Annotations](actions/list-annotations.md) | `GET /app/projects/:projectId/annotations` | [docs](https://developer.mixpanel.com/reference/list-all-annotations-for-project) |
| [List Saved Cohorts](actions/list-saved-cohorts.md) | `POST /query/cohorts/list` | [docs](https://developer.mixpanel.com/reference/cohorts-list) |
| [List Today's Top Events](actions/list-todays-top-events.md) | `GET /query/events/top` | [docs](https://developer.mixpanel.com/reference/query-top-events) |
| [List Top Event Properties](actions/list-top-event-properties.md) | `GET /query/events/properties/top` | [docs](https://developer.mixpanel.com/reference/query-events-top-properties) |
| [List Top Event Property Values](actions/list-top-event-property-values.md) | `GET /query/events/properties/values` | [docs](https://developer.mixpanel.com/reference/query-events-top-property-values) |
| [List Top Events](actions/list-top-events.md) | `GET /query/events/names` | [docs](https://developer.mixpanel.com/reference/query-months-top-event-names) |
| [Query Funnel Report](actions/query-funnel-report.md) | `GET /query/funnels` | [docs](https://developer.mixpanel.com/reference/funnels-query) |
| [Query Profiles](actions/query-profiles.md) | `POST /query/engage` | [docs](https://developer.mixpanel.com/reference/engage-query) |
| [Query Retention Report](actions/query-retention-report.md) | `GET /query/retention` | [docs](https://developer.mixpanel.com/reference/retention-query) |
| [Query Saved Insights Report](actions/query-saved-insights-report.md) | `GET /query/insights` | [docs](https://developer.mixpanel.com/reference/insights-query) |
| [Query Segmentation Report](actions/query-segmentation-report.md) | `GET /query/segmentation` | [docs](https://developer.mixpanel.com/reference/segmentation-query) |
| [Remove from Group List Property](actions/remove-from-group-list-property.md) | `POST https://api.mixpanel.com/groups` | [docs](https://developer.mixpanel.com/reference/group-remove-from-list-property) |
| [Remove from Profile List Property](actions/remove-from-profile-list-property.md) | `POST https://api.mixpanel.com/engage` | [docs](https://developer.mixpanel.com/reference/profile-remove-from-list-property) |
| [Set Group Property Once](actions/set-group-property-once.md) | `POST https://api.mixpanel.com/groups` | [docs](https://developer.mixpanel.com/reference/group-set-property-once) |
| [Set Profile Property](actions/set-profile-property.md) | `POST https://api.mixpanel.com/engage` | [docs](https://developer.mixpanel.com/reference/profile-set) |
| [Set Profile Property Once](actions/set-profile-property-once.md) | `POST https://api.mixpanel.com/engage` | [docs](https://developer.mixpanel.com/reference/profile-set-property-once) |
| [Track Events](actions/track-events.md) | `POST https://api.mixpanel.com/track` | [docs](https://developer.mixpanel.com/reference/track-event) |
| [Union Group List Property](actions/union-group-list-property.md) | `POST https://api.mixpanel.com/groups` | [docs](https://developer.mixpanel.com/reference/group-union) |
| [Union Profile List Property](actions/union-profile-list-property.md) | `POST https://api.mixpanel.com/engage` | [docs](https://developer.mixpanel.com/reference/user-profile-union) |
| [Update Annotation](actions/update-annotation.md) | `PATCH /app/projects/:projectId/annotations/:annotationId` | [docs](https://developer.mixpanel.com/reference/patch-annotation-1) |
| [Update Group Property](actions/update-group-property.md) | `POST https://api.mixpanel.com/groups` | [docs](https://developer.mixpanel.com/reference/group-set-property) |
| [Update Multiple Profiles](actions/update-multiple-profiles.md) | `POST https://api.mixpanel.com/engage` | [docs](https://developer.mixpanel.com/reference/profile-batch-update) |
