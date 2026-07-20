# YouCan: Create Page

Creates a new page in YouCan.

```
POST https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-page', {
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
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "meta": {
        "description": "string",
        "images": [
          "string"
        ],
        "title": "string"
      },
      "name": "Ava Chen",
      "public_url": "https://example.com",
      "slug": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `meta` | object |  |
| `meta.description` | string |  |
| `meta.images` | array |  |
| `meta.title` | string |  |
| `name` | string |  |
| `public_url` | string |  |
| `slug` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native YouCan API, this operation is `POST /pages` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page.md) for the provider-specific parameters and requirements.

