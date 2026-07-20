# ScrapingAnt: Scrape URL With POST

Scrapes a URL with a forwarded POST request in ScrapingAnt.

```
POST https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingAnt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/api"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapingAnt/latest/actions/scrape-url-with-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/api"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Fully qualified URL to scrape with a forwarded POST request. Example: `https://example.com/api`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | Body data to forward with the POST request when the target URL expects a request body. |

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
| `html` | string | Scraped page HTML returned after forwarding the POST request. |

## Native endpoint

Through the native ScrapingAnt API, this operation is `POST /general` (base URL `https://api.scrapingant.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url-with-post.md) for the provider-specific parameters and requirements.

