# WorkflowMax: Create Purchase Order



```
POST https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-purchase-order', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "amountExTax": 1,
      "amountIncTax": 1,
      "costs": [
        {
          "code": "string",
          "costUUID": "string",
          "createdAt": "string",
          "description": "string",
          "jobCostUUID": "string",
          "jobUUID": "string",
          "notes": "string",
          "quantity": 1,
          "tax": [
            {
              "taxName": "Ava Chen",
              "taxRate": 1
            }
          ],
          "type": "string",
          "unitCost": 1,
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "createdAt": "string",
      "date": "string",
      "deliveryAddress": "string",
      "description": "string",
      "jobs": [
        {
          "number": "string",
          "UUID": "string"
        }
      ],
      "purchaseOrderNumber": "string",
      "sent": true,
      "status": "string",
      "supplier": {
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phoneNumber": "string",
        "uuid": "string"
      },
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
| `amountExTax` | number | The total amount of the purchase order excluding tax. |
| `amountIncTax` | number | The total amount of the purchase order including tax. |
| `costs[].code` | string | The code of the cost. |
| `costs[].costUUID` | string | The unique identifier of the cost which is maintained in the cost admin. |
| `costs[].createdAt` | string | The timestamp indicating when the cost item was created. |
| `costs[].description` | string | The description of the cost. |
| `costs[].jobCostUUID` | string | The unique identifier of the job cost. |
| `costs[].jobUUID` | string | The unique identifier of the job which is associated to the cost. |
| `costs[].notes` | string | The notes of the cost. |
| `costs[].quantity` | number | The quantity of the cost. |
| `costs[].tax[].taxName` | string | The name of the tax. |
| `costs[].tax[].taxRate` | number | The rate of the tax. |
| `costs[].type` | string | The type of the cost, it could be service or stock. |
| `costs[].unitCost` | number | The unit cost of the cost. |
| `costs[].updatedAt` | string | The timestamp indicating when the cost item was last updated. |
| `costs[].uuid` | string | The unique identifier of the cost item. |
| `createdAt` | string | The timestamp indicating when the purchase order was created. |
| `date` | string | The date of the purchase order. |
| `deliveryAddress` | string | The delivery address of the purchase order. |
| `description` | string | The description of the purchase order. |
| `jobs[].number` | string | The number of the job. |
| `jobs[].UUID` | string | The unique identifier of the job. |
| `purchaseOrderNumber` | string | The number of the purchase order. |
| `sent` | boolean | Indicate whether the purchase order has been sent or not. |
| `status` | string | The status of the purchase order. |
| `supplier.email` | string | The email address of the supplier. |
| `supplier.name` | string | The name of the supplier. |
| `supplier.phoneNumber` | string | The phone number of the supplier. |
| `supplier.uuid` | string | The unique identifier of the supplier. |
| `updatedAt` | string | The timestamp indicating when the purchase order was last updated. |
| `uuid` | string | The unique identifier of the purchase order. |

## Native endpoint

Through the native WorkflowMax API, this operation is `POST v2/purchase-orders` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.

