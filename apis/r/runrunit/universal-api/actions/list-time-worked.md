# Runrun.it: List Time Worked

Retrieves time worked reports from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-time-worked
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-time-worked?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-time-worked?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeCapacity` | boolean | no | Include capacity |
| `includeUntracked` | boolean | no | Include untracked |
| `includeOthers` | boolean | no | Include others |
| `expandOthers` | boolean | no | Expand others field to a non-aggregate |
| `groupBy` | string | no | Attributes to group by: date, client_id, project_group_id, project_id, project_sub_group_id, task_id, task_status_id, team_id, type_id, user_id |
| `periodType` | string | no | Period type. Must be one of the following: last_seven_days, current_week, last_fifteen_days, last_thirty_days, current_month, last_ninety_days, current_quarter, last_one_year, custom_range |
| `periodStart` | date | no | Period start. Only used if period_type is 'custom_range' |
| `periodEnd` | date | no | Period end. Only used if period_type is 'custom_range' |
| `periodUnit` | string | no | Period unit. Must be one of the following: day, week, month or year |
| `clientId` | string | no | IDs of clients, separated by comma |
| `projectId` | string | no | IDs of projects, separated by comma |
| `projectGroupId` | string | no | ID of project group |
| `projectSubgroupId` | string | no | ID of project subgroup |
| `tagList` | string | no | List of task tags, separated by comma |
| `typeId` | string | no | IDs of task types, separated by comma |
| `teamId` | string | no | IDs of teams, separated by comma |
| `userId` | string | no | IDs of users, separated by comma |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacity": [
        "string"
      ],
      "meta": {},
      "other": [
        "string"
      ],
      "result": [
        "string"
      ],
      "untracked": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity` | array<string> | Total time on users' workweek |
| `meta` | object | Represents the parameters used for building the response |
| `other` | array<string> | Represents all the *other* time worked not contained on the result |
| `result` | array<string> | Time Worked filtered and/or grouped by the given parameters |
| `untracked` | array<string> | Time not tracked by the system |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /reports/time_worked` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-worked.md) for the provider-specific parameters and requirements.

