# Datarobot: List Use Cases

Retrieves a list of use cases from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-use-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-use-cases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-use-cases?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "datasetsCount": 1,
      "deploymentsCount": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectsCount": 1,
      "role": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `datasetsCount` | number |  |
| `deploymentsCount` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectsCount` | number |  |
| `role` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /useCases/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-use-cases.md) for the provider-specific parameters and requirements.

