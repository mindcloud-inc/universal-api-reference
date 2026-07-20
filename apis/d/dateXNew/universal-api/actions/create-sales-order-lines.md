# DateX: Create Sales Order Lines



```
POST https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/create-sales-order-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/create-sales-order-lines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderLines[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/create-sales-order-lines', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderLines[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderLines[]` | array<object> | yes | Array of sales order line objects to create, matching the documented order_lines schema. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "grossWeight": 1,
      "licensePlate": "string",
      "lineNumber": 1,
      "lot": "string",
      "material": "string",
      "netWeight": 1,
      "notes": "string",
      "orderId": 1,
      "packagedAmount": 1,
      "packaging": "string",
      "serialNumber": "string",
      "shipment": "string",
      "status": "string",
      "upc": "string",
      "vendorLot": "string",
      "weightUom": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `grossWeight` | number |  |
| `licensePlate` | string |  |
| `lineNumber` | number |  |
| `lot` | string |  |
| `material` | string |  |
| `netWeight` | number |  |
| `notes` | string |  |
| `orderId` | number |  |
| `packagedAmount` | number |  |
| `packaging` | string |  |
| `serialNumber` | string |  |
| `shipment` | string |  |
| `status` | string |  |
| `upc` | string |  |
| `vendorLot` | string |  |
| `weightUom` | string |  |

## Native endpoint

Through the native DateX API, this operation is `POST sales_order_lines/create` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-order-lines.md) for the provider-specific parameters and requirements.

