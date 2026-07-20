# Brand.dev: Crawl Website Sitemap

Retrieves sitemap data from a website using Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/crawl-website-sitemap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/crawl-website-sitemap?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/crawl-website-sitemap?${params}`, {
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
| `domain` | string | yes | Domain name to crawl the sitemap for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "meta": {
        "errors": 1,
        "sitemapsDiscovered": 1,
        "sitemapsFetched": 1,
        "sitemapsSkipped": 1
      },
      "success": true,
      "urls": [
        [
          "https://example.com"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `meta` | object |  |
| `meta.errors` | number |  |
| `meta.sitemapsDiscovered` | number |  |
| `meta.sitemapsFetched` | number |  |
| `meta.sitemapsSkipped` | number |  |
| `success` | boolean |  |
| `urls[]` | array<string> |  |

## Native endpoint

Through the native Brand.dev API, this operation is `GET /web/scrape/sitemap` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crawl-website-sitemap.md) for the provider-specific parameters and requirements.

