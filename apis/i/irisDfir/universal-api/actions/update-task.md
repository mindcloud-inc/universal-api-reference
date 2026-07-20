# Iris Dfir: Update Task



```
PUT https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Iris Dfir `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "caseIdentifier": 1,
  "identifier": 1,
  "taskAssigneesId[]": [
    1
  ],
  "taskStatusId": 1,
  "taskTitle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "caseIdentifier": 1,
    "identifier": 1,
    "taskAssigneesId[]": [1],
    "taskStatusId": 1,
    "taskTitle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caseIdentifier` | number | yes | IRIS case identifier. |
| `identifier` | number | yes | IRIS task identifier. |
| `taskAssigneesId[]` | array<number> | yes | IRIS task assignee identifier. Accepts multiple values as an array. |
| `taskDescription` | string | no | Optional updated task description. |
| `taskStatusId` | number | yes | IRIS task status identifier. |
| `taskTags` | string | no | Optional updated comma-separated task tags. |
| `taskTitle` | string | yes | Title of the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "case": {
        "case_id": 1,
        "case_name": "Ava Chen"
      },
      "custom_attributes": {},
      "id": 1,
      "modification_history": {},
      "status": {
        "id": 1,
        "status_bscolor": "string",
        "status_description": "string",
        "status_name": "Ava Chen"
      },
      "task_case_id": 1,
      "task_close_date": "2026-05-07T12:00:00.000Z",
      "task_description": "string",
      "task_last_update": "2026-05-07T12:00:00.000Z",
      "task_open_date": "2026-05-07T12:00:00.000Z",
      "task_status_id": 1,
      "task_tags": "string",
      "task_title": "string",
      "task_userid_close": 1,
      "task_userid_open": 1,
      "task_userid_update": 1,
      "task_uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `case.case_id` | number |  |
| `case.case_name` | string |  |
| `custom_attributes` | object |  |
| `id` | number |  |
| `modification_history` | object |  |
| `status.id` | number |  |
| `status.status_bscolor` | string |  |
| `status.status_description` | string |  |
| `status.status_name` | string |  |
| `task_case_id` | number |  |
| `task_close_date` | date |  |
| `task_description` | string |  |
| `task_last_update` | date |  |
| `task_open_date` | date |  |
| `task_status_id` | number |  |
| `task_tags` | string |  |
| `task_title` | string |  |
| `task_userid_close` | number |  |
| `task_userid_open` | number |  |
| `task_userid_update` | number |  |
| `task_uuid` | string |  |

## Native endpoint

Through the native Iris Dfir API, this operation is `PUT /api/v2/cases/:case_identifier/tasks/:identifier` (base URL `https://v200.beta.dfir-iris.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

