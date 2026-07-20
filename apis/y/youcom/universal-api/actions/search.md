# You.com: Search

Retrieves search results from You.com.

```
GET https://connect.mindcloud.co/v1/universal/youcom/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a You.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youcom/latest/actions/search?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youcom/latest/actions/search?${params}`, {
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
| `query` | string | yes | Search query. |
| `count` | number | no | Maximum results per section. |
| `freshness` | string | no | Filter results by recency. |
| `country` | string | no | Country code target. |
| `language` | string | no | BCP 47 language code. |
| `safesearch` | string | no | Safety level. |
| `livecrawl` | string | no | Include full page content. |
| `livecrawlFormats` | string | no | Formats for livecrawl output. |
| `crawlTimeout` | number | no | Livecrawl timeout in seconds. |
| `offset` | number | no | Pagination offset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "latency": 1,
        "query": "string",
        "searchUuid": "string"
      },
      "results": {
        "web": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object | Search metadata. |
| `metadata.latency` | number | Search latency in seconds. |
| `metadata.query` | string | Echoed search query. |
| `metadata.searchUuid` | string | Search request identifier. |
| `results` | object | Top-level search result groups. |
| `results.web[]` | array<object> | Web search result items. |
| `results.web[].description` | string | Short result summary. |
| `results.web[].faviconUrl` | string | Favicon URL for the result domain. |
| `results.web[].originalThumbnailUrl` | string | Original thumbnail image URL when available. |
| `results.web[].pageAge` | date | Page timestamp returned by You.com. |
| `results.web[].snippets[]` | array<string> | Supporting search snippets for the result. |
| `results.web[].thumbnailUrl` | string | Result thumbnail image URL when available. |
| `results.web[].title` | string | Result title. |
| `results.web[].url` | string | Canonical URL for the result page. |

## Native endpoint

Through the native You.com API, this operation is `GET https://ydc-index.io/v1/search` (base URL `https://api.you.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

