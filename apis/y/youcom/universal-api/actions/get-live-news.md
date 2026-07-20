# You.com: Get Live News

Retrieves live news results from You.com.

```
GET https://connect.mindcloud.co/v1/universal/youcom/latest/actions/get-live-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a You.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youcom/latest/actions/get-live-news?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youcom/latest/actions/get-live-news?${params}`, {
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
| `query` | string | yes | News search query. |
| `count` | number | no | Maximum number of news results. |
| `pageNumber` | number | no | Pagination page number. |
| `recency` | string | no | Recency filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "news": {
        "metadata": {
          "requestUuid": "string"
        },
        "query": {
          "original": "string",
          "spellcheckOff": true
        },
        "results": [
          [
            {}
          ]
        ],
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `news` | object | Top-level live news response. |
| `news.metadata` | object | Top-level response metadata. |
| `news.metadata.requestUuid` | string | Request identifier. |
| `news.query` | object | Query details for the live news request. |
| `news.query.original` | string | Original search query. |
| `news.query.spellcheckOff` | boolean | Whether spellcheck was disabled. |
| `news.results[]` | array<object> | Live news result items. |
| `news.results[].age` | string | Relative age label for the article. |
| `news.results[].description` | string | Article summary. |
| `news.results[].metadata` | object | Per-result metadata. |
| `news.results[].metadata.articleId` | string | Article identifier. |
| `news.results[].metaUrl` | object | Parsed article URL metadata. |
| `news.results[].metaUrl.hostname` | string | Article hostname. |
| `news.results[].metaUrl.netloc` | string | Article netloc. |
| `news.results[].metaUrl.path` | string | Article URL path. |
| `news.results[].metaUrl.scheme` | string | Article URL scheme. |
| `news.results[].pageAge` | date | Article timestamp returned by You.com. |
| `news.results[].sourceName` | string | Publisher name. |
| `news.results[].thumbnail` | object | Article thumbnail metadata. |
| `news.results[].thumbnail.src` | string | Article thumbnail URL. |
| `news.results[].title` | string | Article title. |
| `news.results[].type` | string | Result type token. |
| `news.results[].url` | string | Canonical article URL. |
| `news.type` | string | Top-level response type token. |

## Native endpoint

Through the native You.com API, this operation is `GET https://api.ydc-index.io/livenews` (base URL `https://api.you.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-live-news.md) for the provider-specific parameters and requirements.

