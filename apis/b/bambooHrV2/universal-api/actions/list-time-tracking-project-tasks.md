# BambooHR: List Time Tracking Project Tasks

Lists time tracking project tasks from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-time-tracking-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-time-tracking-project-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-time-tracking-project-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The project ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | OData v4 filter expression. Filterable fields: `id`, `name`, `projectId`, `billable`, `createdAt`, `updatedAt`, `deletedAt`. An explicit `deletedAt` predicate overrides the default `statuses[]=active` filter. |
| `sort` | string | no | Sort expression like `name asc, createdAt desc`. Allowed fields: `id`, `name`, `projectId`, `billable`, `createdAt`, `updatedAt`, `deletedAt`. |
| `statuses` | list<string> | no | Statuses to include. Defaults to `active` (excludes deleted tasks). Use both values to include active and deleted tasks. One of: `active`, `deleted`. Accepts multiple values as an array. Default: `[\"active\"]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/time-tracking/projects/:projectId/tasks` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-tracking-project-tasks.md) for the provider-specific parameters and requirements.

