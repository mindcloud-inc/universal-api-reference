# Helpjuice: List Articles

Retrieves articles from Helpjuice.

```
GET https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-articles?${params}`, {
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
| `accessibility` | number | no | Filter articles by accessibility. 1 public, 0 internal, 2 private. |
| `isPublished` | boolean | no | Filter articles by published state. |
| `createdSince` | string | no | Only return articles created on or after this date in dd-mm-yyyy format. |
| `updatedSince` | string | no | Only return articles updated on or after this date in dd-mm-yyyy format. |
| `language` | string | no | Filter articles by language shortcode such as en_us. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles` | array<object> | The Helpjuice articles. |
| `meta` | object | Pagination metadata. |

## Native endpoint

Through the native Helpjuice API, this operation is `GET /articles` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-articles.md) for the provider-specific parameters and requirements.

