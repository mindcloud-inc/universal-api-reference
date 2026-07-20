# retailCRM: Get Task

Retrieves a task from retailCRM by ID.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-task?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-task?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentary": "string",
      "complete": true,
      "createdAt": "string",
      "datetime": "string",
      "id": 1,
      "performer": 1,
      "performerType": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentary` | string |  |
| `complete` | boolean |  |
| `createdAt` | string |  |
| `datetime` | string |  |
| `id` | number |  |
| `performer` | number |  |
| `performerType` | string |  |
| `text` | string |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /tasks/:id` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

