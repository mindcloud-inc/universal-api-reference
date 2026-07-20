# PickFu: Search Help Articles



```
GET https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/search-help-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PickFu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/search-help-articles?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/search-help-articles?${params}`, {
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
| `query` | string | yes | Search query for help articles. |
| `page` | number | no | Page number for help article results. |
| `perPage` | number | no | Number of help article results per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "description": "string",
      "id": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Rendered help article body content. |
| `description` | string | Help article summary text. |
| `id` | string | PickFu help article identifier. |
| `title` | string | Help article title. |
| `url` | string | Canonical PickFu help article URL. |

## Native endpoint

Through the native PickFu API, this operation is `GET /help/search` (base URL `https://api.pickfu.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-help-articles.md) for the provider-specific parameters and requirements.

