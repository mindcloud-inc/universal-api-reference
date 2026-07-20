# WorkflowMax: List Purchase Orders



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-purchase-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-purchase-orders?${params}`, {
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
          "billingStatus": "string",
          "bills": [
            {
              "amountExTax": 1,
              "amountIncTax": 1,
              "createdAt": "string",
              "date": "string",
              "dueDate": "string",
              "receiptDate": "string",
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
          "documents": [
            {
              "createdAt": "string",
              "downloadURL": "https://example.com",
              "fileName": "Ava Chen",
              "fileSize": 1,
              "note": "string",
              "purchaseOrderPhase": "string",
              "title": "string",
              "updatedAt": "string",
              "uploadedByUUID": "string",
              "uuid": "string"
            }
          ],
          "jobs": [
            {
              "jobNumber": "string",
              "jobUUID": "string"
            }
          ],
          "notes": [
            {
              "createdAt": "string",
              "createdByUUID": "string",
              "date": "string",
              "description": "string",
              "phase": "string",
              "title": "string",
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
          "purchaseOrderNumber": "string",
          "sent": true,
          "status": "string",
          "stockReceipts": [
            {
              "amountExTax": 1,
              "amountIncTax": 1,
              "billDate": "string",
              "createdAt": "string",
              "receiptDate": "string",
              "stockReceiptID": "string",
              "stockReceiptNote": "string",
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
          "stockReceiptStatus": "string",
          "supplierUUID": "string",
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
| `data[].amountExTax` | number | The amount excluding tax of the purchase order. |
| `data[].amountIncTax` | number | The amount including tax of the purchase order. |
| `data[].billingStatus` | string | The billing status of the purchase order. |
| `data[].bills[].amountExTax` | number | The amount excluding tax of the purchase order bill. |
| `data[].bills[].amountIncTax` | number | The amount including tax of the purchase order bill. |
| `data[].bills[].createdAt` | string | The UTC date and time when the purchase order bill was created. |
| `data[].bills[].date` | string | The date of the purchase order bill. |
| `data[].bills[].dueDate` | string | The due date of the purchase order bill. |
| `data[].bills[].receiptDate` | string | The receipt date of the stock receipt associated with the purchase order bill. |
| `data[].bills[].stockReceiptID` | string | The ID of the stock receipt associated with the purchase order bill. |
| `data[].bills[].supplierBillNumber` | string | The bill number provided by the supplier for the purchase order bill. |
| `data[].bills[].tax[].taxName` | string | The name of the tax applied to the purchase order stock receipt. |
| `data[].bills[].tax[].taxRate` | number | The tax rate applied to the purchase order stock receipt. |
| `data[].bills[].updatedAt` | string | The UTC date and time when the purchase order bill was last updated. |
| `data[].bills[].uuid` | string | The unique identifier of the purchase order bill. |
| `data[].costs[].code` | string | The code  with the purchase order cost. |
| `data[].costs[].costUUID` | string | unique identifier of the cost associated with the purchase order cost. |
| `data[].costs[].createdAt` | string | The UTC date and time when the purchase order was created. |
| `data[].costs[].description` | string | The description of the purchase order cost. |
| `data[].costs[].jobCostUUID` | string | The unique identifier of the job cost associated with the purchase order cost. |
| `data[].costs[].jobUUID` | string | The unique identifier of the job associated with the purchase order cost. |
| `data[].costs[].notes` | string | Additional notes or comments related to the purchase order cost. |
| `data[].costs[].quantity` | number | The quantity of the purchase order cost. |
| `data[].costs[].tax[].taxName` | string | The name of the tax applied to the purchase order cost. |
| `data[].costs[].tax[].taxRate` | number | The tax rate applied to the purchase order cost. |
| `data[].costs[].type` | string | The type of the purchase order cost, e.g. stock or service. |
| `data[].costs[].unitCost` | number | The unit cost of the purchase order cost. |
| `data[].costs[].updatedAt` | string | The UTC date and time when the purchase order was last updated. |
| `data[].costs[].uuid` | string | The unique identifier of the purchase order cost. |
| `data[].createdAt` | string | The UTC date and time when the purchase order was created. |
| `data[].date` | string | The date of the purchase order. |
| `data[].deliveryAddress` | string | The delivery address of the purchase order. |
| `data[].description` | string | The description of the purchase order. |
| `data[].documents[].createdAt` | string | The UTC date and time when the purchase order document was created. |
| `data[].documents[].downloadURL` | string | The URL for downloading the purchase order document. |
| `data[].documents[].fileName` | string | The file name of the purchase order document. |
| `data[].documents[].fileSize` | number | The file size of the purchase order document. |
| `data[].documents[].note` | string | The note of the purchase order document. |
| `data[].documents[].purchaseOrderPhase` | string | The phase name of the purchase order document. |
| `data[].documents[].title` | string | The title of the purchase order document. |
| `data[].documents[].updatedAt` | string | The UTC date and time when the purchase order document was last updated. |
| `data[].documents[].uploadedByUUID` | string | The unique identifier of the staff who uploaded the purchase order document. |
| `data[].documents[].uuid` | string | The unique identifier for the purchase order document. |
| `data[].jobs[].jobNumber` | string | The job number of the job associated with the purchase order. |
| `data[].jobs[].jobUUID` | string | The unique identifier of the job associated with the purchase order. |
| `data[].notes[].createdAt` | string | The UTC date and time when the purchase order note was created. |
| `data[].notes[].createdByUUID` | string | The unique identifier of the staff who created the purchase order. |
| `data[].notes[].date` | string | The UTC date of the purchase order note. |
| `data[].notes[].description` | string | A description or additional information related to the purchase order note. |
| `data[].notes[].phase` | string | The phase of the purchase order note. |
| `data[].notes[].title` | string | The title of the purchase order note. |
| `data[].notes[].updatedAt` | string | The UTC date and time when the purchase order note was last updated. |
| `data[].notes[].uuid` | string | The unique identifier for the purchase order note. |
| `data[].purchaseOrderNumber` | string | The number of the purchase order. |
| `data[].sent` | boolean | Indicates whether the purchase order was sent. |
| `data[].status` | string | The status of the purchase order. |
| `data[].stockReceipts[].amountExTax` | number | The amount excluding tax of the purchase order stock receipt. |
| `data[].stockReceipts[].amountIncTax` | number | The amount including tax of the purchase order stock receipt. |
| `data[].stockReceipts[].billDate` | string | The bill date of the bill associated with the purchase order stock receipt. |
| `data[].stockReceipts[].createdAt` | string | The UTC date and time when the purchase order stock receipt was created. |
| `data[].stockReceipts[].receiptDate` | string | The receipt date of the purchase order stock receipt. |
| `data[].stockReceipts[].stockReceiptID` | string | The ID of the purchase order stock receipt. |
| `data[].stockReceipts[].stockReceiptNote` | string | The receipt note of the purchase order stock receipt. |
| `data[].stockReceipts[].supplierBillNumber` | string | The bill number provided by the supplier for the purchase order stock receipt. |
| `data[].stockReceipts[].tax[].taxName` | string | The name of the tax applied to the purchase order stock receipt. |
| `data[].stockReceipts[].tax[].taxRate` | number | The tax rate applied to the purchase order stock receipt. |
| `data[].stockReceipts[].updatedAt` | string | The UTC date and time when the purchase order stock receipt was last updated. |
| `data[].stockReceipts[].uuid` | string | The unique identifier of the purchase order stock receipt. |
| `data[].stockReceiptStatus` | string | The stock receipt status of the purchase order. |
| `data[].supplierUUID` | string | The unique identifier of the supplier for the purchase order. |
| `data[].updatedAt` | string | The UTC date and time when the purchase order was last updated. |
| `data[].uuid` | string | The unique identifier of the purchase order. |
| `total` | number | The total number of purchase orders returned. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/purchase-orders` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchase-orders.md) for the provider-specific parameters and requirements.

