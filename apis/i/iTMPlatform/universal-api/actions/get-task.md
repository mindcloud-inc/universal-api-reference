# ITM Platform: Get Task



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-task?connectionId=$CONNECTION_ID&projectId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | The ITM Platform task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": "string",
      "id": 1,
      "kanbanId": 1,
      "kindId": 1,
      "name": "Ava Chen",
      "no": "string",
      "projectId": 1,
      "status": {}
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
| `kanbanId` | number |  |
| `kindId` | number |  |
| `name` | string |  |
| `no` | string |  |
| `projectId` | number |  |
| `status` | object |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /Projects/{ProjectId}/Tasks/{TaskId}` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

