# LinkAce: Create Tag

Creates a new tag in LinkAce.

```
POST https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkAce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
      "id": 1,
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
| `id` | number | Unique tag identifier. |
| `name` | string | Tag name. |
| `updated_at` | string | Last update timestamp. |
| `user_id` | number | Owning user identifier. |
| `visibility` | number | Visibility value for the tag. |

## Native endpoint

Through the native LinkAce API, this operation is `POST /tags` (base URL `https://demo.linkace.org/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

