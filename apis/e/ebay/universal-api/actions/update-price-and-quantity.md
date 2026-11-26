# eBay: Update - Price and Quantity



```
PUT https://connect.mindcloud.co/v1/universal/ebay/latest/actions/update-price-and-quantity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/update-price-and-quantity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ebay/latest/actions/update-price-and-quantity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requests[].shipToLocationAvailability` | object | no |  |
| `requests[].shipToLocationAvailability.quantity` | number | no |  |
| `requests[].sku` | string | no |  |
| `requests[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native eBay API, this operation is `POST sell/inventory/v1/bulk_update_price_quantity` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-price-and-quantity.md) for the provider-specific parameters and requirements.

