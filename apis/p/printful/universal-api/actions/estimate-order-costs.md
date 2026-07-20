# Printful: Estimate Order Costs

Estimates costs for a Printful order draft.

```
GET https://connect.mindcloud.co/v1/universal/printful/latest/actions/estimate-order-costs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printful/latest/actions/estimate-order-costs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printful/latest/actions/estimate-order-costs?${params}`, {
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
      "costs": {},
      "retail_costs": {},
      "shipments": [
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
| `costs` | object |  |
| `retail_costs` | object |  |
| `shipments` | array<object> |  |

## Native endpoint

Through the native Printful API, this operation is `POST /orders/estimate-costs` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-order-costs.md) for the provider-specific parameters and requirements.

