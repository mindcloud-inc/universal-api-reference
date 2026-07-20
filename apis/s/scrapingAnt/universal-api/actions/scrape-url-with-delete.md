# ScrapingAnt: Scrape URL With DELETE

Scrapes a URL with a forwarded DELETE request in ScrapingAnt.

```
DELETE https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-delete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingAnt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-delete?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fapi%2Fitem%2F123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/api/item/123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-delete?${params}`, {
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
| `url` | string | yes | Fully qualified URL to scrape with a forwarded DELETE request. Example: `https://example.com/api/item/123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | Body data to forward with the DELETE request when the target URL expects a request body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Scraped page HTML returned after forwarding the DELETE request. |

## Native endpoint

Through the native ScrapingAnt API, this operation is `DELETE /general` (base URL `https://api.scrapingant.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url-with-delete.md) for the provider-specific parameters and requirements.

