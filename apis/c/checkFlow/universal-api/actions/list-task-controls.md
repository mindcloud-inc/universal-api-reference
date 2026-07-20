# CheckFlow: List Task Controls



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-task-controls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-task-controls?connectionId=$CONNECTION_ID&taskKey=07072bc4-f1eb-4536-819a-1ddb7dc109a1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskKey": "07072bc4-f1eb-4536-819a-1ddb7dc109a1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-task-controls?${params}`, {
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
| `taskKey` | string | yes | The key of the task. Use Get Template Tasks to find the key. Example: `07072bc4-f1eb-4536-819a-1ddb7dc109a1`. |
| `contentType` | string | no | Filters results by control type. Use ALL to return every control. Example: `ALLINPUT`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/template/task-content` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-controls.md) for the provider-specific parameters and requirements.

