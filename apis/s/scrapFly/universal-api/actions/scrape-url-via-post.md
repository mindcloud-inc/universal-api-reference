# ScrapFly: Scrape URL via POST

Creates a new page scrape in ScrapFly.

```
POST https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url-via-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url-via-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://httpbin.dev/anything"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url-via-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://httpbin.dev/anything"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | Raw request body to forward to the target URL. |
| `url` | string | yes | Target URL to scrape with a POST request. Example: `https://httpbin.dev/anything`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {
        "method": "string",
        "project": "string",
        "url": "https://example.com"
      },
      "result": {
        "contentType": "string",
        "logUrl": "https://example.com",
        "statusCode": 1,
        "success": true,
        "url": "https://example.com"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config.method` | string | HTTP method used for the scrape request. |
| `config.project` | string | ScrapFly project name. |
| `config.url` | string | Requested target URL. |
| `result.contentType` | string | Returned content type. |
| `result.logUrl` | string | ScrapFly dashboard log URL. |
| `result.statusCode` | number | Upstream HTTP status code. |
| `result.success` | boolean | Whether the scrape completed successfully. |
| `result.url` | string | Resolved target URL. |
| `uuid` | string | Scrape run UUID. |

## Native endpoint

Through the native ScrapFly API, this operation is `POST /scrape` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url-via-post.md) for the provider-specific parameters and requirements.

