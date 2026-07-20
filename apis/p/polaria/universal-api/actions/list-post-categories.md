# Polaria: List Post Categories

Retrieves post categories from Polaria.

```
GET https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-post-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polaria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-post-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-post-categories?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "parent": 1,
      "slug": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | number |  |
| `parent` | number |  |
| `slug` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Polaria API, this operation is `GET /faq_categories` (base URL `https://app.polaria.ai/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-post-categories.md) for the provider-specific parameters and requirements.

