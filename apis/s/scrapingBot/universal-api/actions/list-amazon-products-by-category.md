# ScrapingBot: List Amazon Products by Category



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-amazon-products-by-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-amazon-products-by-category?connectionId=$CONNECTION_ID&category_id=13896617011" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category_id": "13896617011"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-amazon-products-by-category?${params}`, {
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
| `category_id` | string | yes | Amazon category identifier. Default: `13896617011`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "data": {},
      "duration": "string",
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
| `status` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /amazon` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-amazon-products-by-category.md) for the provider-specific parameters and requirements.

