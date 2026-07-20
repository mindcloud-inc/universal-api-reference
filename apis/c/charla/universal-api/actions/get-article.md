# Charla: Get Article

Retrieves an article from Charla.

```
GET https://connect.mindcloud.co/v1/universal/charla/latest/actions/get-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Charla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charla/latest/actions/get-article?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/charla/latest/actions/get-article?${params}`, {
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
| `id` | number | yes | The article ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "article": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "slug": "string",
      "status": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `article` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native Charla API, this operation is `GET /kb/articles/:id` (base URL `https://api.charla.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article.md) for the provider-specific parameters and requirements.

