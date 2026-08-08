# Fraser Direct: Create purchase order



```
POST https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fraser Direct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "poDate": "2024-12-20",
  "vendorNumber": "string",
  "detailList[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/create-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "poDate": "2024-12-20",
    "vendorNumber": "string",
    "detailList[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `poDate` | string | yes | Required purchase order date in YYYY-MM-DD format. Example: `2024-12-20`. |
| `vendorNumber` | string | yes | Required vendor number validated against Fraser Direct ERP. |
| `depositorOrderNumber` | string | no | DepositorOrderNumber or ShipmentIdentificationNumber must be provided. |
| `shipmentIdentificationNumber` | string | no | DepositorOrderNumber or ShipmentIdentificationNumber must be provided. |
| `priority` | list | no | Optional priority. Valid values are RUSH or empty. One of: `0`, `1`. |
| `detailList[]` | array<object> | yes | Required array of purchase-order line objects. Each line should include LineNumber, QuantityShipped, optional UOM, required SKU, and optional VendorLineNumber. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "depositorOrderNumber": "string",
      "poStatus": "string",
      "shipmentIdentificationNumber": "string",
      "success": "string",
      "validationResults": [
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
| `depositorOrderNumber` | string |  |
| `poStatus` | string |  |
| `shipmentIdentificationNumber` | string |  |
| `success` | string |  |
| `validationResults` | array<object> |  |

## Native endpoint

Through the native Fraser Direct API, this operation is `POST /CreatePO` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.

