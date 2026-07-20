# YouCan: Get Page

Retrieves details for a page from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-page?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-page?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

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

Through the native YouCan API, this operation is `GET /pages/{id}` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

