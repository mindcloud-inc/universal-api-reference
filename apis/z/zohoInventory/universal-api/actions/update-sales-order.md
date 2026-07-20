# Zoho Inventory: Update Sales Order

Updates an existing sales order in Zoho Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "salesOrderId": "string",
  "organizationId": "{{credentials.organizationId}}",
  "customerId": "string",
  "salesOrderNumber": "string",
  "lineItems[]": [
    {}
  ],
  "lineItems[].itemId": "string",
  "lineItems[].quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "salesOrderId": "string",
    "organizationId": "{{credentials.organizationId}}",
    "customerId": "string",
    "salesOrderNumber": "string",
    "lineItems[]": [{}],
    "lineItems[].itemId": "string",
    "lineItems[].quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `salesOrderId` | string | yes | The Zoho Inventory salesorder_id for the sales order. |
| `organizationId` | string | yes | Zoho Inventory organization ID to run this request against. Default: `{{credentials.organizationId}}`. |
| `customerId` | string | yes | Customer to bill on the sales order. |
| `salesOrderNumber` | string | yes | Unique number for the sales order. |
| `date` | string | no | Sales order date in YYYY-MM-DD format. |
| `referenceNumber` | string | no | External reference number for the sales order. |
| `notes` | string | no | Notes shown on the sales order. |
| `lineItems[]` | array<object> | yes | One or more sales order line items. |
| `lineItems[].lineItemId` | string | no | Existing line item identifier when updating a line. |
| `lineItems[].itemId` | string | yes | Item to set on this line. |
| `lineItems[].quantity` | number | yes | Quantity to order for this line. |
| `lineItems[].rate` | number | no | Rate for this line item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "created_time": "string",
      "customer_id": "string",
      "customer_name": "Ava Chen",
      "date": "string",
      "last_modified_time": "string",
      "line_items": [
        {}
      ],
      "notes": "string",
      "order_status": "string",
      "packages": [
        {}
      ],
      "reference_number": "string",
      "salesorder_id": "string",
      "salesorder_number": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `created_time` | string |  |
| `customer_id` | string |  |
| `customer_name` | string |  |
| `date` | string |  |
| `last_modified_time` | string |  |
| `line_items` | array<object> |  |
| `notes` | string |  |
| `order_status` | string |  |
| `packages` | array<object> |  |
| `reference_number` | string |  |
| `salesorder_id` | string |  |
| `salesorder_number` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Zoho Inventory API, this operation is `PUT /salesorders/:salesorder_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-order.md) for the provider-specific parameters and requirements.

