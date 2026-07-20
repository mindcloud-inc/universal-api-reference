# ITM Platform: List Agile Task Statuses



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-agile-task-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-agile-task-statuses?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-agile-task-statuses?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "date": "string",
      "default": true,
      "id": 1,
      "kanbanId": 1,
      "name": "Ava Chen",
      "order": 1,
      "type": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `date` | string |  |
| `default` | boolean |  |
| `id` | number |  |
| `kanbanId` | number |  |
| `name` | string |  |
| `order` | number |  |
| `type` | object |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /v2/Projects/{ProjectId}/GetKanbanTaskStatus` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agile-task-statuses.md) for the provider-specific parameters and requirements.

