# LinkAce: Get List

Retrieves a specific list from LinkAce.

```
GET https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkAce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/get-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/get-list?${params}`, {
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
      "created_at": "string",
      "deleted_at": "string",
      "description": "string",
      "id": 1,
      "links": "https://example.com",
      "name": "Ava Chen",
      "updated_at": "string",
      "user_id": 1,
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Creation timestamp. |
| `deleted_at` | string | Deletion timestamp when present. |
| `description` | string | List description. |
| `id` | number | Unique list identifier. |
| `links` | string | API URL for the links in this list. |
| `name` | string | List name. |
| `updated_at` | string | Last update timestamp. |
| `user_id` | number | Owning user identifier. |
| `visibility` | number | Visibility value for the list. |

## Native endpoint

Through the native LinkAce API, this operation is `GET /lists/{list_id}` (base URL `https://demo.linkace.org/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

