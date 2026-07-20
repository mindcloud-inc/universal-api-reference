# Kadoa: Start Crawl



```
POST https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/start-crawl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/start-crawl" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/start-crawl', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL to crawl Default: `https://example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxPages` | number | no | Maximum pages to crawl Default: `10`. |
| `maxDepth` | number | no | Maximum crawl depth Default: `3`. |
| `strictDomain` | boolean | no | Only crawl within same domain Default: `true`. |
| `proxyType` | string | no | Proxy type to use |
| `proxyCountry` | string | no | Proxy country ISO code |
| `timeout` | number | no | Timeout in milliseconds Default: `30000`. |
| `callbackUrl` | string | no | Webhook URL for completion callback |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configId": "string",
      "error": "string",
      "message": "string",
      "sessionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configId` | string |  |
| `error` | string |  |
| `message` | string |  |
| `sessionId` | string |  |

## Native endpoint

Through the native Kadoa API, this operation is `POST /v4/crawl/` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-crawl.md) for the provider-specific parameters and requirements.

