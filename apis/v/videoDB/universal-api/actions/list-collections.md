# VideoDB: List Collections

Retrieves collections from VideoDB.

```
GET https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VideoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/list-collections?${params}`, {
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
      "description": "string",
      "id": "string",
      "is_public": true,
      "name": "Ava Chen",
      "owner": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Collection description. |
| `id` | string | Collection identifier. |
| `is_public` | boolean | Whether the collection is public. |
| `name` | string | Collection name. |
| `owner` | string | Owner identifier. |

## Native endpoint

Through the native VideoDB API, this operation is `GET /collection/` (base URL `https://api.videodb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

