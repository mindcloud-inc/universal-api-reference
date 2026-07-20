# Iris Dfir: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Iris Dfir `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&caseIdentifier=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "caseIdentifier": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-tasks?${params}`, {
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
| `caseIdentifier` | number | yes | IRIS case identifier. |

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

Through the native Iris Dfir API, this operation is `GET /api/v2/cases/:case_identifier/tasks` (base URL `https://v200.beta.dfir-iris.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

