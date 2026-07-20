# Langbase: Search Web



```
GET https://connect.mindcloud.co/v1/universal/langbase/latest/actions/search-web
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/search-web?connectionId=$CONNECTION_ID&webSearchKey=string&query=string&service=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webSearchKey": "string",
  "query": "string",
  "service": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/search-web?${params}`, {
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
| `webSearchKey` | string | yes | Langbase web search key for the `LB-WEB-SEARCH-KEY` request header. |
| `query` | string | yes | Search query to run. |
| `service` | list | yes | Web search provider service. One of: `0`. |
| `totalResults` | number | no | Maximum number of search results to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Langbase API returns.

## Native endpoint

Through the native Langbase API, this operation is `POST v1/tools/web-search` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-web.md) for the provider-specific parameters and requirements.

