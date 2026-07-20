# WorkflowMax: List Purchase Order Bills



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-purchase-order-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-purchase-order-bills?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-purchase-order-bills?${params}`, {
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
      "data": [
        {
          "amountExTax": 1,
          "amountIncTax": 1,
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
          "date": "string",
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].amountExTax` | number | The amount excluding tax of the bill. |
| `data[].amountIncTax` | number | The amount including tax of the bill. |
| `data[].costs[].additional` | boolean | Indicate whether the cost item is additional in the purchase order. |
| `data[].costs[].createdAt` | string | The date and time when the cost item was created. |
| `data[].costs[].name` | string | The name of the cost item. |
| `data[].costs[].purchaseOrderCostUUID` | string | The unique identifier of the purchase order cost associated with the cost item. |
| `data[].costs[].quantity` | number | The quantity of the cost item. |
| `data[].costs[].tax[].taxName` | string | The date and time when the cost item was created. |
| `data[].costs[].tax[].taxRate` | number | The date and time when the cost item was last updated. |
| `data[].costs[].unitCost` | number | The unit cost of the cost item. |
| `data[].costs[].updatedAt` | string | The date and time when the cost item was last updated. |
| `data[].costs[].uuid` | string | The unique identifier of the cost item. |
| `data[].createdAt` | string | The UTC date and time when the bill was created. |
| `data[].date` | string | The date of the bill. |
| `data[].dueDate` | string | The due date of the bill. |
| `data[].purchaseOrderUUID` | string | The unique identifier of the purchase order associated with the bill. |
| `data[].receiptDate` | string | The receipt date of the stock receipt linked to the bill. |
| `data[].status` | string | The status of the bill, e.g. approved, cancelled. |
| `data[].stockReceiptID` | string | The ID of the stock receipt linked to the bill. |
| `data[].supplierBillNumber` | string | The bill number issued by the supplier of the bill. |
| `data[].tax[].taxName` | string | The tax name of the tax applied to the bill. |
| `data[].tax[].taxRate` | number | The tax rate of the tax applied to the bill. |
| `data[].updatedAt` | string | The UTC date and time when the bill was last updated. |
| `data[].uuid` | string | The unique identifier of the bill. |
| `total` | number | The total number of bills returned. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/purchase-orders/bills` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchase-order-bills.md) for the provider-specific parameters and requirements.

