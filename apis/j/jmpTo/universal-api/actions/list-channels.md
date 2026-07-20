# JmpTo: List Channels

Retrieves channels from JmpTo.

```
GET https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-channels?${params}`, {
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
      "color": "string",
      "date": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "starred": true
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
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `starred` | boolean |  |

## Native endpoint

Through the native JmpTo API, this operation is `GET /channels` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

