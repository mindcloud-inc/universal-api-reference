# Shopkit: Get Stats

Retrieves store statistics from Shopkit.

```
GET https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/get-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/get-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/get-stats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "abandon_rate": 1,
      "abandoned_cart_total": 1,
      "abandoned_total_carts": 1,
      "abandoned_total_items": 1,
      "conversion_rate": 1,
      "date_end_raw": "2026-05-07T12:00:00.000Z",
      "date_start_raw": "2026-05-07T12:00:00.000Z",
      "direct_traffic": 1,
      "order_avg_value": 1,
      "orders_count": 1,
      "orders_revenue": 1,
      "products_sold": 1,
      "referral_traffic": 1,
      "search_keywords": [
        {}
      ],
      "search_traffic": 1,
      "sessions": 1,
      "websites_referral": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abandon_rate` | number |  |
| `abandoned_cart_total` | number |  |
| `abandoned_total_carts` | number |  |
| `abandoned_total_items` | number |  |
| `conversion_rate` | number |  |
| `date_end_raw` | date |  |
| `date_start_raw` | date |  |
| `direct_traffic` | number |  |
| `order_avg_value` | number |  |
| `orders_count` | number |  |
| `orders_revenue` | number |  |
| `products_sold` | number |  |
| `referral_traffic` | number |  |
| `search_keywords` | array<object> |  |
| `search_traffic` | number |  |
| `sessions` | number |  |
| `websites_referral` | array<object> |  |

## Native endpoint

Through the native Shopkit API, this operation is `GET /stats` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stats.md) for the provider-specific parameters and requirements.

