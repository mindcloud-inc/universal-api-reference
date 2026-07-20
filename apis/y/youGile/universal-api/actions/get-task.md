# YouGile: Get task

Retrieves details for a task from YouGile.

```
GET https://connect.mindcloud.co/v1/universal/youGile/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouGile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youGile/latest/actions/get-task?${params}`, {
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
| `id` | string | yes | The YouGile task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "columnId": "string",
      "completed": true,
      "createdBy": "string",
      "deadline": {},
      "deleted": true,
      "description": "string",
      "id": "string",
      "idTaskCommon": "string",
      "idTaskProject": "string",
      "stickers": {},
      "timestamp": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `columnId` | string |  |
| `completed` | boolean |  |
| `createdBy` | string |  |
| `deadline` | object |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `idTaskCommon` | string |  |
| `idTaskProject` | string |  |
| `stickers` | object |  |
| `timestamp` | number |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native YouGile API, this operation is `GET /tasks/:id` (base URL `{{credentials.companyDomain}}/api-v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

