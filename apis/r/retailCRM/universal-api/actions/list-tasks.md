# retailCRM: List Tasks

Retrieves tasks from retailCRM.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native retailCRM API, this operation is `GET /tasks` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

