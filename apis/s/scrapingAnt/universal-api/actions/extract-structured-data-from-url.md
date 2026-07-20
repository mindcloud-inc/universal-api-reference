# ScrapingAnt: Extract Structured Data From URL

Retrieves AI-extracted structured data from a URL in ScrapingAnt.

```
GET https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/extract-structured-data-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingAnt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/extract-structured-data-from-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fproduct&extractProperties=product%20title%2C%20price(number)%2C%20full%20description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/product",
  "extractProperties": "product title, price(number), full description"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/extract-structured-data-from-url?${params}`, {
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
| `url` | string | yes | Fully qualified URL to scrape and extract structured data from. Example: `https://example.com/product`. |
| `extractProperties` | string | yes | Free-form description of the fields to extract, such as "product title, price(number), full description". Example: `product title, price(number), full description`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `browser` | boolean | no | Enable ScrapingAnt headless browser rendering. Default is true. |
| `timeout` | number | no | Maximum request runtime in seconds. ScrapingAnt supports 5-60 seconds. Example: `30`. |
| `proxyType` | list<string> | no | Proxy pool type. Supported values are datacenter and residential. One of: `datacenter`, `residential`. |
| `proxyCountry` | string | no | Two-letter proxy country code, such as US, GB, BR, or DE. Example: `US`. |
| `waitForSelector` | string | no | CSS selector ScrapingAnt should wait for before returning the result. Requires browser=true. Example: `.product`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapingAnt API returns.

## Native endpoint

Through the native ScrapingAnt API, this operation is `GET /extract` (base URL `https://api.scrapingant.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-structured-data-from-url.md) for the provider-specific parameters and requirements.

