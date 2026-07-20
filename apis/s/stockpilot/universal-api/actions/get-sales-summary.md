# Stockpilot: Get Sales Summary

Retrieves sales summary analytics from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-sales-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-sales-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-sales-summary?${params}`, {
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
| `range` | number | no | Default: `14`. |
| `topItems` | number | no | Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "period": {
        "days": 1,
        "end_date": "2026-05-07T12:00:00.000Z",
        "start_date": "2026-05-07T12:00:00.000Z"
      },
      "summary": {
        "average_order_value": 1,
        "total_items_sold": 1,
        "total_orders": 1,
        "total_revenue": 1,
        "unique_products_sold": 1
      },
      "top_selling_items": [
        [
          {}
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
| `period.days` | number |  |
| `period.end_date` | date |  |
| `period.start_date` | date |  |
| `summary.average_order_value` | number |  |
| `summary.total_items_sold` | number |  |
| `summary.total_orders` | number |  |
| `summary.total_revenue` | number |  |
| `summary.unique_products_sold` | number |  |
| `top_selling_items[]` | array<object> |  |
| `top_selling_items[].total_orders` | number |  |
| `top_selling_items[].total_revenue` | number |  |
| `top_selling_items[].total_sold` | number |  |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /analytics/sales-summary` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-summary.md) for the provider-specific parameters and requirements.

