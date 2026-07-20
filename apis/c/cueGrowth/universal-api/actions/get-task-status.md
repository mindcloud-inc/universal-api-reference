# CueGrowth: Get Task Status



```
GET https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/get-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/get-task-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/get-task-status?${params}`, {
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
| `id` | string | yes | ID of the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native CueGrowth API, this operation is `GET /tasks/{id}/status` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-status.md) for the provider-specific parameters and requirements.

