# Walmart: List Items - Simulation

Retrieve all items from a partner’s catalog in the Dynamic Sandbox.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-items-simulation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-items-simulation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-items-simulation?${params}`, {
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
      "gtin": "string",
      "lifecycleStatus": "string",
      "mart": "string",
      "price": {
        "amount": 1,
        "currency": "string"
      },
      "productName": "Ava Chen",
      "productType": "string",
      "publishedStatus": "string",
      "shelf": "string",
      "sku": "string",
      "upc": "string",
      "wpid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gtin` | string |  |
| `lifecycleStatus` | string |  |
| `mart` | string |  |
| `price.amount` | number |  |
| `price.currency` | string |  |
| `productName` | string |  |
| `productType` | string |  |
| `publishedStatus` | string |  |
| `shelf` | string |  |
| `sku` | string |  |
| `upc` | string |  |
| `wpid` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v1/simulations/items` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items-simulation.md) for the provider-specific parameters and requirements.

