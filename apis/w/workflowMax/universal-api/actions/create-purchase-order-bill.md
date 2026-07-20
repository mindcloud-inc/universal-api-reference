# WorkflowMax: Create Purchase Order Bill



```
POST https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-purchase-order-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-purchase-order-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrderIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-purchase-order-bill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaseOrderIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrderIdentifier` | string | yes | The WorkflowMax purchase order identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountExTax": 1,
      "amountIncTax": 1,
      "billDate": "string",
      "costs": [
        {
          "additional": true,
          "createdAt": "string",
          "name": "Ava Chen",
          "purchaseOrderCostUUID": "string",
          "quantity": 1,
          "tax": [
            {
              "taxName": "Ava Chen",
              "taxRate": 1
            }
          ],
          "unitCost": 1,
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "createdAt": "string",
      "dueDate": "string",
      "purchaseOrderUUID": "string",
      "receiptDate": "string",
      "status": "string",
      "stockReceiptID": "string",
      "supplierBillNumber": "string",
      "tax": [
        {
          "taxName": "Ava Chen",
          "taxRate": 1
        }
      ],
      "updatedAt": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountExTax` | number | Total bill amount excluding tax, represented in the smallest currency unit (e.g., cents). |
| `amountIncTax` | number | Total bill amount including tax, represented in the smallest currency unit. |
| `billDate` | string | Date the bill was generated, formatted as YYYY-MM-DD. |
| `costs[].additional` | boolean | Indicate whether the bill cost item is additional or not. |
| `costs[].createdAt` | string | The UTC timestamp indicating when the bill cost item was created. |
| `costs[].name` | string | Name of the bill cost item. |
| `costs[].purchaseOrderCostUUID` | string | Unique identifier of the associated purchase order cost item. |
| `costs[].quantity` | number | Quantity of the bill cost item. |
| `costs[].tax[].taxName` | string | The name or description of the tax applied to the billed amount |
| `costs[].tax[].taxRate` | number | The percentage rate at which tax is applied to the billed item or service |
| `costs[].unitCost` | number | The pre-tax unit cost of the bill cost item. |
| `costs[].updatedAt` | string | The UTC timestamp indicating when the bill cost item was last updated. |
| `costs[].uuid` | string | Unique identifier for the bill cost item. |
| `createdAt` | string | The UTC timestamp indicating when the bill  was created. |
| `dueDate` | string | Payment deadline for the bill, formatted as YYYY-MM-DD. |
| `purchaseOrderUUID` | string | UUID of the purchase order linked to this bill. |
| `receiptDate` | string | The date of the stock receipt linked to the bill. Format: YYYY-MM-DD. |
| `status` | string | Current status of the bill’s processing lifecycle, i.e. approved or cancelled. |
| `stockReceiptID` | string | ID of the stock receipt linked to the bill. |
| `supplierBillNumber` | string | Official supplier bill number used for reference and tracking. |
| `tax[].taxName` | string | Name or description of the tax applied to the bill. |
| `tax[].taxRate` | number | Applicable tax rate for the bill, expressed as a percentage. |
| `updatedAt` | string | The UTC timestamp indicating when the bill was last updated. |
| `uuid` | string | Unique identifier for the bill. |

## Native endpoint

Through the native WorkflowMax API, this operation is `POST v2/purchase-orders/{identifier}/bills` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order-bill.md) for the provider-specific parameters and requirements.

