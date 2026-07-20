# Mews: Get All Tasks

Retrieves tasks from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-tasks?${params}`, {
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
| `taskIds[]` | array<string> | no | Optional task identifiers to fetch specific tasks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closedUtc": "2026-05-07T12:00:00.000Z",
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "deadlineUtc": "2026-05-07T12:00:00.000Z",
      "departmentId": "string",
      "description": "string",
      "enterpriseId": "string",
      "id": "string",
      "name": "Ava Chen",
      "serviceOrderId": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closedUtc` | date | Closed timestamp in UTC when present. |
| `createdUtc` | date | Creation timestamp in UTC. |
| `deadlineUtc` | date | Deadline timestamp in UTC. |
| `departmentId` | string | Department identifier when present. |
| `description` | string | Task description when present. |
| `enterpriseId` | string | Enterprise identifier. |
| `id` | string | Unique identifier of the task. |
| `name` | string | Task name. |
| `serviceOrderId` | string | Service order identifier when present. |
| `state` | string | Current task state. |

## Native endpoint

Through the native Mews API, this operation is `POST /tasks/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-tasks.md) for the provider-specific parameters and requirements.

