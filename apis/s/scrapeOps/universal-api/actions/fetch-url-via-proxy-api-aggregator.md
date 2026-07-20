# ScrapeOps: Fetch Url Via Proxy Api Aggregator

Fetches a URL through the ScrapeOps proxy aggregator.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/fetch-url-via-proxy-api-aggregator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/fetch-url-via-proxy-api-aggregator?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/fetch-url-via-proxy-api-aggregator?${params}`, {
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
| `url` | string | yes | The URL to fetch through the ScrapeOps Proxy API Aggregator. |
| `renderJs` | boolean | no | Enable JavaScript rendering for the target page. |
| `residential` | boolean | no | Use residential proxies for the request. |
| `country` | string | no | Two-letter country code for geotargeting. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeOps API returns.

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-url-via-proxy-api-aggregator.md) for the provider-specific parameters and requirements.

