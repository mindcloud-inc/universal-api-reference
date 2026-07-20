# JmpTo: List Pixels

Retrieves pixels from JmpTo.

```
GET https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-pixels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-pixels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-pixels?${params}`, {
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
      "date": "string",
      "id": 1,
      "name": "Ava Chen",
      "tag": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `id` | number |  |
| `name` | string |  |
| `tag` | string |  |
| `type` | string |  |

## Native endpoint

Through the native JmpTo API, this operation is `GET /pixels` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pixels.md) for the provider-specific parameters and requirements.

