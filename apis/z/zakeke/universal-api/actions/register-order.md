# Zakeke: Register Order



```
POST https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/register-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zakeke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/register-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderCode": "ORD-1001",
  "orderDate": "2026-03-19T10:30:00Z",
  "details[].orderDetailCode": "line-1",
  "total": "149.99",
  "details[].sku": "SKU-001",
  "details[].designId": "000-RE1olDzbT234viB6D11a10",
  "details[].modelUnitPrice": "99.99",
  "details[].designUnitPrice": "50.00",
  "details[].quantity": "1",
  "compositionDetails[].orderDetailCode": "line-2",
  "compositionDetails[].compositionId": "000-RE1olDzbT234viB6D11a10",
  "compositionDetails[].unitPrice": "149.99",
  "compositionDetails[].quantity": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/register-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderCode": "ORD-1001",
    "orderDate": "2026-03-19T10:30:00Z",
    "details[].orderDetailCode": "line-1",
    "total": "149.99",
    "details[].sku": "SKU-001",
    "details[].designId": "000-RE1olDzbT234viB6D11a10",
    "details[].modelUnitPrice": "99.99",
    "details[].designUnitPrice": "50.00",
    "details[].quantity": "1",
    "compositionDetails[].orderDetailCode": "line-2",
    "compositionDetails[].compositionId": "000-RE1olDzbT234viB6D11a10",
    "compositionDetails[].unitPrice": "149.99",
    "compositionDetails[].quantity": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderCode` | string | yes | Unique identifier of the order on the ecommerce. Example: `ORD-1001`. |
| `orderDate` | string | yes | Order date in ISO 8601 format. Example: `2026-03-19T10:30:00Z`. |
| `customerCode` | string | no | Registered customer identifier from the ecommerce system. Example: `customer-001`. |
| `details[].orderDetailCode` | string | yes | The ID on your system for the customized-product line item. Example: `line-1`. |
| `total` | number | yes | The total order amount in the base currency set in Zakeke API settings. Example: `149.99`. |
| `details` | list<object> | no | List of customized product details. Example: `At least one customized line item when the order contains designs.`. |
| `details[].sku` | string | yes | Unique identifier that the ordered customized product has in ecommerce. Example: `SKU-001`. |
| `details[].designId` | string | yes | Unique design identifier provided by Zakeke. Example: `000-RE1olDzbT234viB6D11a10`. |
| `details[].modelUnitPrice` | number | yes | Product unit price without the design price. Example: `99.99`. |
| `details[].designUnitPrice` | number | yes | Unit price applied to customization. Example: `50.00`. |
| `details[].quantity` | number | yes | Quantity of products ordered. Example: `1`. |
| `compositionDetails[].orderDetailCode` | string | yes | The ID on your system for the configured-product line item. Example: `line-2`. |
| `compositionDetails` | list<object> | no | List of configured product details. Example: `Configured-product line items when the order contains compositions.`. |
| `compositionDetails[].compositionId` | string | yes | The product configuration identifier for the configured product that the line item belongs to. Example: `000-RE1olDzbT234viB6D11a10`. |
| `compositionDetails[].unitPrice` | number | yes | The unit price of the configured product including configuration price after discounts. Example: `149.99`. |
| `compositionDetails[].quantity` | number | yes | The number of configured products that were purchased. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `visitorCode` | string | no | Visitor identifier from the ecommerce system when there is no registered customer. Example: `visitor-001`. |
| `sessionId` | string | no | The ecommerce session identifier. Example: `sess_12345`. |
| `details[].designModificationId` | string | no | Identifier assigned by Zakeke for a specific Names and Numbers or bulk-variation instance. Example: `mod_001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "marketplaceID": 1,
      "orderCode": "string",
      "orderDate": "string",
      "sessionID": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `marketplaceID` | number |  |
| `orderCode` | string |  |
| `orderDate` | string |  |
| `sessionID` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Zakeke API, this operation is `POST /v2/order` (base URL `https://api.zakeke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-order.md) for the provider-specific parameters and requirements.

