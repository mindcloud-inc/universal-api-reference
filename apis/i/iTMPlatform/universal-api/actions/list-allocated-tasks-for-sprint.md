# ITM Platform: List Allocated Tasks For Sprint



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-allocated-tasks-for-sprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-allocated-tasks-for-sprint?connectionId=$CONNECTION_ID&projectId=string&sprintId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "sprintId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-allocated-tasks-for-sprint?${params}`, {
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
| `projectId` | string | yes | The ITM Platform project ID. |
| `sprintId` | string | yes | The ITM Platform sprint ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": "string",
      "id": 1,
      "jiraId": 1,
      "name": "Ava Chen",
      "no": "string",
      "projectId": 1,
      "status": {},
      "swimlane": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | string |  |
| `id` | number |  |
| `jiraId` | number |  |
| `name` | string |  |
| `no` | string |  |
| `projectId` | number |  |
| `status` | object |  |
| `swimlane` | object |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /v2/Projects/{ProjectId}/AllocatedTasks/{SprintId}` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-allocated-tasks-for-sprint.md) for the provider-specific parameters and requirements.

