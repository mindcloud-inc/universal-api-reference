# Tettra: Search Pages

Finds pages in Tettra by search term.

```
GET https://connect.mindcloud.co/v1/universal/tettra/latest/actions/search-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tettra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tettra/latest/actions/search-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tettra/latest/actions/search-pages?${params}`, {
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
| `query` | string | no | Search term. Leave empty to return recent pages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pages": [
        {
          "category": {
            "id": 1,
            "name": "Ava Chen",
            "url": "https://example.com"
          },
          "content": "string",
          "id": 1,
          "owner": "string",
          "title": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      ],
      "query": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pages[].category.id` | number |  |
| `pages[].category.name` | string |  |
| `pages[].category.url` | string |  |
| `pages[].content` | string |  |
| `pages[].id` | number |  |
| `pages[].owner` | string |  |
| `pages[].title` | string |  |
| `pages[].updated_at` | date |  |
| `pages[].url` | string |  |
| `query` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tettra API, this operation is `GET /teams/85329/search` (base URL `https://app.tettra.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-pages.md) for the provider-specific parameters and requirements.

