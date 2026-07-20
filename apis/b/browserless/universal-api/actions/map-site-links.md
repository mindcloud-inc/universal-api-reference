# Browserless: Map Site Links

Retrieves discovered site links from Browserless.

```
GET https://connect.mindcloud.co/v1/universal/browserless/latest/actions/map-site-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browserless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserless/latest/actions/map-site-links?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserless/latest/actions/map-site-links?${params}`, {
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
| `url` | string | yes | The base URL to crawl for links. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | string | no | Optional query used to rank mapped links by relevance. |
| `limit` | number | no | Optional maximum number of links to return. |
| `sitemap` | string | no | Controls sitemap behavior. Valid values are `include`, `only`, and `skip`. |
| `includeSubdomains` | boolean | no | Whether to include URLs from subdomains. |
| `ignoreQueryParameters` | boolean | no | Whether to exclude URLs that include query parameters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        "https://example.com"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | array<string> | URLs returned by Browserless for the requested site map run. |
| `success` | boolean | Whether Browserless completed the site map request successfully. |

## Native endpoint

Through the native Browserless API, this operation is `POST /map` (base URL `https://production-sfo.browserless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/map-site-links.md) for the provider-specific parameters and requirements.

