# ScrapingBot: Search Amazon Products



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/search-amazon-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/search-amazon-products?connectionId=$CONNECTION_ID&query=laptop" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "laptop"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/search-amazon-products?${params}`, {
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
| `query` | string | yes | Search keyword or phrase. Default: `laptop`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "data": {},
      "duration": "string",
      "parameters": {},
      "request_id": "string",
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `data` | object |  |
| `duration` | string |  |
| `parameters` | object |  |
| `request_id` | string |  |
| `status` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /amazon` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-amazon-products.md) for the provider-specific parameters and requirements.

