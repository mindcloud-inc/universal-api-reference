# Browserless: Search Web

Retrieves web search results from Browserless.

```
GET https://connect.mindcloud.co/v1/universal/browserless/latest/actions/search-web
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browserless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserless/latest/actions/search-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserless/latest/actions/search-web?${params}`, {
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
| `query` | string | yes | The web search query to run. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Optional maximum number of search results to return. |
| `categories[]` | array<string> | no | Optional category filters. Valid values are `github`, `pdf`, and `research`. |
| `sources[]` | array<string> | no | Optional source filters. Valid values are `images`, `news`, and `web`. |
| `tbs` | string | no | Optional time-based filter for the search results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Search result groups returned by Browserless. |
| `success` | boolean | Whether Browserless completed the web search request successfully. |
| `totalResults` | number | Total number of search results reported by Browserless. |

## Native endpoint

Through the native Browserless API, this operation is `POST /search` (base URL `https://production-sfo.browserless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-web.md) for the provider-specific parameters and requirements.

