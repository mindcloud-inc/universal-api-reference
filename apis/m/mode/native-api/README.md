# Mode: Native API Reference

A consolidated summary of Mode's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://mode.com/developer/api-reference/introduction/
- **API base URL:** `https://app.mode.com/api/{workspace}`

## Authentication

### Workspace API Token

Authenticate with a Mode Workspace API token using HTTP Basic auth.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Workspace Slug:** `workspace` · required · Mode workspace slug used in API paths, for example mindcloud.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://mode.com/developer/api-reference/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/hal+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | `POST /spaces` | [docs](https://mode.com/developer/api-reference/management/collections/) |
| [Create Collection Membership](actions/create-collection-membership.md) | `POST /spaces/[:space]/memberships` | [docs](https://mode.com/developer/api-reference/management/space-memberships/) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://mode.com/developer/api-reference/management/groups/) |
| [Create Group Membership](actions/create-group-membership.md) | `POST /groups/[:groupToken]/memberships` | [docs](https://mode.com/developer/api-reference/management/group-memberships/) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /spaces/[:space]` | [docs](https://mode.com/developer/api-reference/management/collections/) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/[:groupToken]` | [docs](https://mode.com/developer/api-reference/management/groups/) |
| [Delete Group Membership](actions/delete-group-membership.md) | `DELETE /groups/[:groupToken]/memberships/[:membershipToken]` | [docs](https://mode.com/developer/api-reference/management/group-memberships/) |
| [Get Collection](actions/get-collection.md) | `GET /spaces/[:space]` | [docs](https://mode.com/developer/api-reference/management/collections/) |
| [Get Collection Membership](actions/get-collection-membership.md) | `GET /spaces/[:space]/memberships/[:spaceMembership]` | [docs](https://mode.com/developer/api-reference/management/space-memberships/) |
| [Get Group](actions/get-group.md) | `GET /groups/[:groupToken]` | [docs](https://mode.com/developer/api-reference/management/groups/) |
| [Get Group Membership](actions/get-group-membership.md) | `GET /groups/[:groupToken]/memberships/[:membershipToken]` | [docs](https://mode.com/developer/api-reference/management/group-memberships/) |
| [List Collection Memberships](actions/list-collection-memberships.md) | `GET /spaces/[:space]/memberships` | [docs](https://mode.com/developer/api-reference/management/space-memberships/) |
| [List Collections](actions/list-collections.md) | `GET /spaces` | [docs](https://mode.com/developer/api-reference/management/collections/) |
| [List Data Sources](actions/list-data-sources.md) | `GET /data_sources` | [docs](https://mode.com/developer/api-reference/management/data-sources/) |
| [List Group Memberships](actions/list-group-memberships.md) | `GET /groups/[:groupToken]/memberships` | [docs](https://mode.com/developer/api-reference/management/group-memberships/) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://mode.com/developer/api-reference/management/groups/) |
| [List Reports For Collection](actions/list-reports-for-collection.md) | `GET /spaces/[:space]/reports` | [docs](https://mode.com/developer/api-reference/analytics/reports/) |
| [List Workspace Memberships](actions/list-workspace-memberships.md) | `GET /memberships` | [docs](https://mode.com/developer/api-reference/management/workspace-memberships/) |
| [Retrieve Audit Logs](actions/retrieve-audit-logs.md) | `GET /audit_logs` | [docs](https://mode.com/developer/api-reference/management/audit-logs/) |
| [Update Collection](actions/update-collection.md) | `PATCH /spaces/[:space]` | [docs](https://mode.com/developer/api-reference/management/collections/) |
| [Update Group](actions/update-group.md) | `PATCH /groups/[:groupToken]` | [docs](https://mode.com/developer/api-reference/management/groups/) |
