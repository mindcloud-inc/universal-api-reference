# DialMyCalls: List Groups

Retrieves a list of groups from DialMyCalls.

```
GET https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DialMyCalls `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-groups?${params}`, {
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
      "contactsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactsCount` | number |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native DialMyCalls API, this operation is `GET /groups` (base URL `https://{{credentials.apiKey}}@api.dialmycalls.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

