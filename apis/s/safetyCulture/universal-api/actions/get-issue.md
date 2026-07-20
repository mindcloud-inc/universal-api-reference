# SafetyCulture: Get Issue

Retrieves an issue from SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-issue?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-issue?${params}`, {
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
| `id` | string | yes | Required. The unique ID of the incident to retrieve. Can either be a uuid or a org level unique incident id. Example: IS-4352 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string",
      "task": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "dueAt": "2026-05-07T12:00:00.000Z",
        "priorityId": "string",
        "statusId": "string",
        "taskId": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string |  |
| `task.createdAt` | date |  |
| `task.description` | string |  |
| `task.dueAt` | date |  |
| `task.priorityId` | string |  |
| `task.statusId` | string |  |
| `task.taskId` | string |  |
| `task.title` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `GET /tasks/v1/incident/{id}` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue.md) for the provider-specific parameters and requirements.

