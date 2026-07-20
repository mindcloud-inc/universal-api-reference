# Usedesk: List Articles

Retrieves a list of knowledge base articles from Usedesk.

```
GET https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-articles?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-articles?${params}`, {
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
| `articleIds` | string | no | Article IDs, separated by commas. |
| `categoryIds` | string | no | Category IDs, separated by commas. |
| `collectionIds` | string | no | Section IDs, separated by commas. |
| `order` | string | no | Sort order: asc or desc. |
| `query` | string | no | Search string for article title and text. |
| `sort` | string | no | Sort field. |
| `type` | string | no | Filter by article visibility: public or private. |
| `count` | number | no | Number of articles per page. |
| `page` | number | no | Page number. |
| `shortText` | number | no | Return trimmed search results when query is provided. |

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

Through the native Usedesk API, this operation is `GET /support/:account_id/articles/list` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-articles.md) for the provider-specific parameters and requirements.

