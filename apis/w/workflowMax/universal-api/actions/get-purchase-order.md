# WorkflowMax: Get Purchase Order



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-purchase-order?connectionId=$CONNECTION_ID&purchaseOrderIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseOrderIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-purchase-order?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

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
      "billingStatus": "string",
      "bills": [
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
                  "taxRate": 1,
                  "taxType": "string"
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
          "uploadedBy": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
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
          "comments": [
            {
              "comment": "string",
              "createdAt": "string",
              "createdBy": {
                "firstName": "Ava",
                "lastName": "Chen",
                "uuid": "string"
              },
              "updatedAt": "string"
            }
          ],
          "createdAt": "string",
          "createdBy": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
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
          "costs": [
            {
              "additional": true,
              "createdAt": "string",
              "name": "Ava Chen",
              "purchaseOrderCostUUID": "string",
              "quantity": 1,
              "taxRate": [
                {
                  "taxName": "Ava Chen",
                  "taxRate": 1,
                  "taxType": "string"
                }
              ],
              "unitCost": 1,
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
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
| `amountExTax` | number | The amount excluding tax of the purchase order. |
| `amountIncTax` | number | The amount including tax of the purchase order. |
| `billingStatus` | string | The billing status of the purchase order, e.g. awaiting, partial, full. |
| `bills[].amountExTax` | number | The amount excluding tax of the bill. |
| `bills[].amountIncTax` | number | The amount including tax of the bill. |
| `bills[].costs[].additional` | boolean | Indicate whether the bill cost item is additional in the purchase order. |
| `bills[].costs[].createdAt` | string | The date and time when the bill cost item was created. |
| `bills[].costs[].name` | string | The name of the bill cost item. |
| `bills[].costs[].purchaseOrderCostUUID` | string | The unique identifier of the purchase order cost associated with the bill cost item. |
| `bills[].costs[].quantity` | number | The quantity of bill cost item. |
| `bills[].costs[].tax[].taxName` | string | The name of the tax applied to the bill cost item. |
| `bills[].costs[].tax[].taxRate` | number | The tax rate of the tax applied to the bill cost item. |
| `bills[].costs[].tax[].taxType` | string | The type of the tax applied to the bill cost item. |
| `bills[].costs[].unitCost` | number | The unit cost of bill cost item. |
| `bills[].costs[].updatedAt` | string | The date and time when the bill cost item was last updated. |
| `bills[].costs[].uuid` | string | The unique identifier of the bill cost item. |
| `bills[].createdAt` | string | The UTC date and time when the bill was created. |
| `bills[].date` | string | The date when the bill is issued. |
| `bills[].dueDate` | string | The due date for the purchase order bill. |
| `bills[].receiptDate` | string | The receipt date of the stock receipt linked to the bill. |
| `bills[].stockReceiptID` | string | The ID of the stock receipt linked to the bill. |
| `bills[].supplierBillNumber` | string | The bill number from the supplier related to the bill. |
| `bills[].tax[].taxName` | string | The name of the tax applied to the bill. |
| `bills[].tax[].taxRate` | number | The tax rate of the tax applied to the bill. |
| `bills[].updatedAt` | string | The UTC date and time when the bill was last updated. |
| `bills[].uuid` | string | The unique identifier of the bill. |
| `costs[].code` | string | The code of the purchase order. |
| `costs[].costUUID` | string | The unique identifier of the cost associated with the purchase order cost. |
| `costs[].createdAt` | string | The UTC date and time when the purchase order cost was created. |
| `costs[].description` | string | The description of the purchase order cost. |
| `costs[].jobCostUUID` | string | The unique identifier of the job cost associated with the purchase order cost. |
| `costs[].jobUUID` | string | The unique identifier of the job associated with the purchase order cost. |
| `costs[].notes` | string | Additional notes or comments related to the purchase order cost. |
| `costs[].quantity` | number | The quantity of the purchase order cost. |
| `costs[].tax[].taxName` | string | The name of the tax applied to the purchase order cost. |
| `costs[].tax[].taxRate` | number | The tax rate applied to the purchase order cost. |
| `costs[].type` | string | The type of the purchase order cost, e.g. stock or service. |
| `costs[].unitCost` | number | The unit cost of the purchase order cost. |
| `costs[].updatedAt` | string | The UTC date and time when the purchase order cost was last updated. |
| `costs[].uuid` | string | The unique identifier of the purchase order cost. |
| `createdAt` | string | The UTC date and time when the purchase order was created. |
| `date` | string | The date of the purchase order. |
| `deliveryAddress` | string | The delivery address of the purchase order. |
| `description` | string | The description of the purchase order. |
| `documents[].createdAt` | string | The UTC date and time when the purchase order document was created. |
| `documents[].downloadURL` | string | The URL for downloading the purchase order document. |
| `documents[].fileName` | string | The file name of the purchase order document. |
| `documents[].fileSize` | number | The file size of the purchase order document. |
| `documents[].note` | string | The note of the purchase order document. |
| `documents[].purchaseOrderPhase` | string | The phase name of the purchase order document. |
| `documents[].title` | string | The title of the purchase order document. |
| `documents[].updatedAt` | string | The UTC date and time when the purchase order document was last updated. |
| `documents[].uploadedBy.firstName` | string | The first name of the staff who uploaded the purchase order document. |
| `documents[].uploadedBy.lastName` | string | The last name of the staff who uploaded the purchase order document. |
| `documents[].uploadedBy.uuid` | string | The unique identifier of the staff who uploaded the purchase order document. |
| `documents[].uuid` | string | The unique identifier of the purchase order document. |
| `jobs[].jobNumber` | string | The job number of the job for the purchase order. |
| `jobs[].jobUUID` | string | The unique identifier of the job for the purchase order. |
| `notes[].comments[].comment` | string | The detailed comment of the purchase order note comment. |
| `notes[].comments[].createdAt` | string | The timestamp when the purchase order note comment was created. |
| `notes[].comments[].createdBy.firstName` | string | The first name of the staff who created the purchase order note comment. |
| `notes[].comments[].createdBy.lastName` | string | The last name of the staff who created the purchase order note comment. |
| `notes[].comments[].createdBy.uuid` | string | The unique identifier of the staff who created the purchase order note comment. |
| `notes[].comments[].updatedAt` | string | The timestamp when the purchase order note comment was last updated. |
| `notes[].createdAt` | string | The UTC date and time when the purchase order note was created. |
| `notes[].createdBy.firstName` | string | The first name of the staff who created the purchase order note. |
| `notes[].createdBy.lastName` | string | The last name of the staff who created the purchase order. note |
| `notes[].createdBy.uuid` | string | The unique identifier of the staff who created the purchase order note. |
| `notes[].date` | string | The UTC date of the purchase order note. |
| `notes[].description` | string | A description or additional information related to the purchase order note. |
| `notes[].phase` | string | The phase name of the purchase order note. |
| `notes[].title` | string | The title of the purchase order note. |
| `notes[].updatedAt` | string | The UTC date and time when the purchase order note was last updated. |
| `notes[].uuid` | string | The unique identifier of the purchase order note. |
| `purchaseOrderNumber` | string | The number of the purchase order. |
| `sent` | boolean | Indicate whether the purchase order has been sent to the client. |
| `status` | string | The status of the purchase order, e.g. draft, issued, cancelled. |
| `stockReceipts[].amountExTax` | number | The amount excluding tax of the purchase order stock receipt. |
| `stockReceipts[].amountIncTax` | number | The amount including tax of the purchase order stock receipt. |
| `stockReceipts[].billDate` | string | The bill date associated with the purchase order stock receipt. |
| `stockReceipts[].costs[].additional` | boolean | Indicate whether the stock receipt cost is additional in purchase order. |
| `stockReceipts[].costs[].createdAt` | string | The date and time when the stock receipt cost item was created. |
| `stockReceipts[].costs[].name` | string | The name of the stock receipt cost item. |
| `stockReceipts[].costs[].purchaseOrderCostUUID` | string | The unique identifier of the purchase order cost associated with the stock receipt cost item. |
| `stockReceipts[].costs[].quantity` | number | The quantity of the stock receipt cost item. |
| `stockReceipts[].costs[].taxRate[].taxName` | string | The name of the tax applied to the stock receipt cost item. |
| `stockReceipts[].costs[].taxRate[].taxRate` | number | The tax rate applied to the stock receipt cost item. |
| `stockReceipts[].costs[].taxRate[].taxType` | string | The tax type of the stock receipt cost item. |
| `stockReceipts[].costs[].unitCost` | number | The unit cost of the stock receipt cost item. |
| `stockReceipts[].costs[].updatedAt` | string | The date and time when the stock receipt cost item was last updated. |
| `stockReceipts[].costs[].uuid` | string | The unique identifier of the stock receipt cost item. |
| `stockReceipts[].createdAt` | string | The UTC date and time when the stock receipt was created. |
| `stockReceipts[].receiptDate` | string | The date when the purchase order stock receipt was issued. |
| `stockReceipts[].stockReceiptID` | string | The ID of the purchase order stock receipt. |
| `stockReceipts[].stockReceiptNote` | string | Notes related to the purchase order stock receipt. |
| `stockReceipts[].supplierBillNumber` | string | The bill number associated with the purchase order stock receipt. |
| `stockReceipts[].tax[].taxName` | string | The name of the tax applied to the purchase order cost. |
| `stockReceipts[].tax[].taxRate` | number | The tax rate applied to the purchase order cost. |
| `stockReceipts[].updatedAt` | string | The UTC date and time when the stock receipt was last updated. |
| `stockReceipts[].uuid` | string | The unique identifier of the stock receipt. |
| `stockReceiptStatus` | string | The stock receipt status of the purchase order, e.g. awaiting, partial, full. |
| `supplier.email` | string | The email of the supplier for the purchase order. |
| `supplier.name` | string | The name of the supplier for the purchase order. |
| `supplier.phoneNumber` | string | The phone number of the supplier for the purchase order. |
| `supplier.uuid` | string | The unique identifier of the supplier for the purchase order. |
| `updatedAt` | string | The UTC date and time when the purchase order was last updated. |
| `uuid` | string | The unique identifier of the purchase order. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/purchase-orders/{identifier}` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order.md) for the provider-specific parameters and requirements.

