# Stockpilot: Get Item Sales Analytics

Retrieves item sales analytics from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-item-sales-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-item-sales-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-item-sales-analytics?${params}`, {
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
| `id` | number | no |  |
| `sku` | string | no |  |
| `barcode` | string | no |  |
| `range` | number | no | Default: `14`. |
| `includeChannels` | boolean | no | Default: `false`. |
| `metrics` | string | no | Default: `all`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "daily_breakdown": [
        [
          {}
        ]
      ],
      "forecast": {
        "daily_forecast": 1,
        "method": "string",
        "monthly_forecast": 1,
        "weekly_forecast": 1
      },
      "item": {
        "backorder_amount": 1,
        "current_stock": 1,
        "id": 1,
        "product_name": "Ava Chen",
        "sku": "string"
      },
      "period": {
        "days": 1,
        "end_date": "2026-05-07T12:00:00.000Z",
        "start_date": "2026-05-07T12:00:00.000Z"
      },
      "pricing": {
        "average_selling_price": 1,
        "highest_selling_price": 1,
        "lowest_selling_price": 1
      },
      "revenue": {
        "average_order_value": 1,
        "total_revenue": 1
      },
      "total_items_sold": 1,
      "total_orders": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `daily_breakdown[]` | array<object> |  |
| `forecast.daily_forecast` | number |  |
| `forecast.method` | string |  |
| `forecast.monthly_forecast` | number |  |
| `forecast.weekly_forecast` | number |  |
| `item.backorder_amount` | number |  |
| `item.current_stock` | number |  |
| `item.id` | number |  |
| `item.product_name` | string |  |
| `item.sku` | string |  |
| `period.days` | number |  |
| `period.end_date` | date |  |
| `period.start_date` | date |  |
| `pricing.average_selling_price` | number |  |
| `pricing.highest_selling_price` | number |  |
| `pricing.lowest_selling_price` | number |  |
| `revenue.average_order_value` | number |  |
| `revenue.total_revenue` | number |  |
| `total_items_sold` | number |  |
| `total_orders` | number |  |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /analytics/items/sales` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-sales-analytics.md) for the provider-specific parameters and requirements.

