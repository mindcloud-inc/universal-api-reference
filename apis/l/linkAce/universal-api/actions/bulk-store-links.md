# LinkAce: Bulk Store Links

Creates multiple bookmark links in LinkAce.

```
POST https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/bulk-store-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkAce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/bulk-store-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/bulk-store-links', {
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
      "check_disabled": true,
      "created_at": "string",
      "deleted_at": "string",
      "description": "string",
      "icon": "string",
      "id": 1,
      "lists": [
        {}
      ],
      "status": 1,
      "tags": [
        {}
      ],
      "title": "string",
      "updated_at": "string",
      "url": "https://example.com",
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
| `check_disabled` | boolean | Whether link checking is disabled. |
| `created_at` | string | Creation timestamp. |
| `deleted_at` | string | Deletion timestamp when present. |
| `description` | string | Bookmark description. |
| `icon` | string | Link icon class or value. |
| `id` | number | Unique link identifier. |
| `lists` | array<object> | Lists attached to the link. |
| `status` | number | Status value for the link. |
| `tags` | array<object> | Tags attached to the link. |
| `title` | string | Bookmark title. |
| `updated_at` | string | Last update timestamp. |
| `url` | string | Stored bookmark URL. |
| `user_id` | number | Owning user identifier. |
| `visibility` | number | Visibility value for the link. |

## Native endpoint

Through the native LinkAce API, this operation is `POST /bulk/links` (base URL `https://demo.linkace.org/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-store-links.md) for the provider-specific parameters and requirements.

