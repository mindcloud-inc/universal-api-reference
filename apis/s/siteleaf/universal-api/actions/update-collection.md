# Siteleaf: Update Collection

Updates an existing collection in Siteleaf.

```
PUT https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/update-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/update-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/update-collection', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionPath` | string | no | Collection path slug |
| `siteId` | string | no | Siteleaf site identifier |
| `title` | string | no | Updated collection title |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "directory": "string",
      "id": "string",
      "metadata": {},
      "output": true,
      "path": "string",
      "permalink": "https://example.com",
      "site_id": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `directory` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `output` | boolean |  |
| `path` | string |  |
| `permalink` | string |  |
| `site_id` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `user_id` | string |  |

## Native endpoint

Through the native Siteleaf API, this operation is `PUT /sites/:site_id/collections/:path` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection.md) for the provider-specific parameters and requirements.

