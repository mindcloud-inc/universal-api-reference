# Usedesk: Get Article

Retrieves a knowledge base article by ID from Usedesk.

```
GET https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/get-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/get-article?connectionId=$CONNECTION_ID&accountId=1&articleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "articleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/get-article?${params}`, {
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
| `accountId` | number | yes | Knowledge base ID in the system. |
| `articleId` | number | yes | Article ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category_id": 1,
      "collection_id": 1,
      "created_at": "string",
      "id": 1,
      "is_rating": 1,
      "order": 1,
      "public": 1,
      "rating": {},
      "text": "string",
      "title": "string",
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category_id` | number |  |
| `collection_id` | number |  |
| `created_at` | string |  |
| `id` | number |  |
| `is_rating` | number |  |
| `order` | number |  |
| `public` | number |  |
| `rating` | object |  |
| `text` | string |  |
| `title` | string |  |
| `views` | number |  |

## Native endpoint

Through the native Usedesk API, this operation is `GET /support/:account_id/articles/:id` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article.md) for the provider-specific parameters and requirements.

