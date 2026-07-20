# Runrun.it: List Project Sub Groups

Retrieves project subgroups from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-project-sub-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-project-sub-groups?connectionId=$CONNECTION_ID&limit=25&offset=0&projectGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-project-sub-groups?${params}`, {
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
| `projectGroupId` | string | yes | Project Group Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": 1,
      "activities_0_days_ago": 1,
      "activities_1_days_ago": 1,
      "activities_2_days_ago": 1,
      "activities_3_days_ago": 1,
      "activities_4_days_ago": 1,
      "activities_5_days_ago": 1,
      "activities_6_days_ago": 1,
      "client_id": 1,
      "client_name": "Ava Chen",
      "cost_pending": 1,
      "cost_total": 1,
      "cost_worked": 1,
      "id": 1,
      "is_default": true,
      "name": "Ava Chen",
      "project_group_id": 1,
      "project_group_is_default": true,
      "project_group_name": "Ava Chen",
      "projects_count": 1,
      "time_pending": 1,
      "time_pending_backlog": 1,
      "time_pending_not_assigned": 1,
      "time_pending_queued": 1,
      "time_progress": 1,
      "time_total": 1,
      "time_worked": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | number |  |
| `activities_0_days_ago` | number |  |
| `activities_1_days_ago` | number |  |
| `activities_2_days_ago` | number |  |
| `activities_3_days_ago` | number |  |
| `activities_4_days_ago` | number |  |
| `activities_5_days_ago` | number |  |
| `activities_6_days_ago` | number |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `cost_pending` | number |  |
| `cost_total` | number |  |
| `cost_worked` | number |  |
| `id` | number |  |
| `is_default` | boolean |  |
| `name` | string |  |
| `project_group_id` | number |  |
| `project_group_is_default` | boolean |  |
| `project_group_name` | string |  |
| `projects_count` | number |  |
| `time_pending` | number |  |
| `time_pending_backlog` | number |  |
| `time_pending_not_assigned` | number |  |
| `time_pending_queued` | number |  |
| `time_progress` | number |  |
| `time_total` | number |  |
| `time_worked` | number |  |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /project_groups/:project_group_id/project_sub_groups` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-sub-groups.md) for the provider-specific parameters and requirements.

