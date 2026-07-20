# Sponsy: Get Customer Metrics

Retrieves customer metrics from Sponsy.

```
GET https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/get-customer-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/get-customer-metrics?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/get-customer-metrics?${params}`, {
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
| `customerId` | string | yes | Customer ID from Sponsy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averageRevenuePerSlot": 1,
      "totalRevenue": 1,
      "totalSlots": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageRevenuePerSlot` | number |  |
| `totalRevenue` | number |  |
| `totalSlots` | number |  |

## Native endpoint

Through the native Sponsy API, this operation is `GET /v1/customers/:customerId/metrics` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-metrics.md) for the provider-specific parameters and requirements.

