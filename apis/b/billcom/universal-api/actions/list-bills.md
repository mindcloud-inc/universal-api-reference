# BILL Payables & Receivables: List Bills

Retrieves bills from Bill.com.

```
GET https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Payables & Receivables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-bills?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-bills?${params}`, {
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
| `filters[]` | array | no |  |
| `filters[].field` | string | no |  |
| `filters[].comparison` | list | no |  |
| `filters[].value` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acctEntityId": "string",
      "actgClassId": "string",
      "amount": 1,
      "apAccountId": "string",
      "approvalStatus": "string",
      "billLineItems": [
        {
          "acctEntityId": "string",
          "actgClassId": "string",
          "amortizationScheduleId": "string",
          "amount": 1,
          "billedUnitPrice": {},
          "billId": "string",
          "chartOfAccountId": "string",
          "createdTime": "string",
          "customerId": "string",
          "departmentId": "string",
          "description": {},
          "employeeId": "string",
          "endDate": {},
          "entity": "string",
          "form1099CategoryId": "string",
          "id": "string",
          "isReportable": true,
          "itemId": "string",
          "jobBillable": true,
          "jobId": "string",
          "jobTaskId": "string",
          "lineOrder": 1,
          "lineType": "string",
          "locationId": "string",
          "purchaseOrderBillLinkId": "https://example.com",
          "quantity": {},
          "reportableAmount": {},
          "startDate": {},
          "unitOfMeasureId": "string",
          "unitPrice": {},
          "updatedTime": "string"
        }
      ],
      "billLocationId": "string",
      "billTemplateId": "string",
      "chartOfAccountId": "string",
      "createdBy": "string",
      "createdTime": "string",
      "creditAmount": 1,
      "defaultInvoiceNumber": true,
      "departmentId": "string",
      "description": {},
      "discountAmount": {},
      "discountDueDate": {},
      "discountStatus": "string",
      "dueAmount": 1,
      "dueDate": "string",
      "eBillCreated": true,
      "entity": "string",
      "exchangeRate": {},
      "expense": {
        "count": 1,
        "totalAmount": 1
      },
      "fullPaymentDate": "string",
      "glPostingDate": "string",
      "hasAmortizedLines": true,
      "hasAutoPay": true,
      "hasLinkedPurchaseOrders": true,
      "id": "string",
      "invoiceDate": "string",
      "invoiceNumber": "string",
      "invoiceProductId": "string",
      "is1099MissingBill": true,
      "isActive": "string",
      "isAutoSaved": true,
      "isSppCreated": true,
      "isVcardStpCandidate": true,
      "item": {
        "count": 1,
        "totalAmount": 1
      },
      "lastPaymentDate": "string",
      "localAmount": {},
      "locationId": "string",
      "multipleBillLineItems": true,
      "numApprPolicyEx": 1,
      "organizationName": "Ava Chen",
      "orgId": "string",
      "paidAmount": 1,
      "payFromBankAccountId": "string",
      "payFromChartOfAccountId": "string",
      "paymentStatus": "string",
      "paymentTermId": "string",
      "poNumber": "string",
      "quickbooksId": {},
      "scheduledAmount": 1,
      "source": "string",
      "uiPaymentStatus": "string",
      "updatedTime": "string",
      "useBillDesc": true,
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acctEntityId` | string |  |
| `actgClassId` | string |  |
| `amount` | number |  |
| `apAccountId` | string |  |
| `approvalStatus` | string |  |
| `billLineItems[].acctEntityId` | string |  |
| `billLineItems[].actgClassId` | string |  |
| `billLineItems[].amortizationScheduleId` | string |  |
| `billLineItems[].amount` | number |  |
| `billLineItems[].billedUnitPrice` | object |  |
| `billLineItems[].billId` | string |  |
| `billLineItems[].chartOfAccountId` | string |  |
| `billLineItems[].createdTime` | string |  |
| `billLineItems[].customerId` | string |  |
| `billLineItems[].departmentId` | string |  |
| `billLineItems[].description` | object |  |
| `billLineItems[].employeeId` | string |  |
| `billLineItems[].endDate` | object |  |
| `billLineItems[].entity` | string |  |
| `billLineItems[].form1099CategoryId` | string |  |
| `billLineItems[].id` | string |  |
| `billLineItems[].isReportable` | boolean |  |
| `billLineItems[].itemId` | string |  |
| `billLineItems[].jobBillable` | boolean |  |
| `billLineItems[].jobId` | string |  |
| `billLineItems[].jobTaskId` | string |  |
| `billLineItems[].lineOrder` | number |  |
| `billLineItems[].lineType` | string |  |
| `billLineItems[].locationId` | string |  |
| `billLineItems[].purchaseOrderBillLinkId` | string |  |
| `billLineItems[].quantity` | object |  |
| `billLineItems[].reportableAmount` | object |  |
| `billLineItems[].startDate` | object |  |
| `billLineItems[].unitOfMeasureId` | string |  |
| `billLineItems[].unitPrice` | object |  |
| `billLineItems[].updatedTime` | string |  |
| `billLocationId` | string |  |
| `billTemplateId` | string |  |
| `chartOfAccountId` | string |  |
| `createdBy` | string |  |
| `createdTime` | string |  |
| `creditAmount` | number |  |
| `defaultInvoiceNumber` | boolean |  |
| `departmentId` | string |  |
| `description` | object |  |
| `discountAmount` | object |  |
| `discountDueDate` | object |  |
| `discountStatus` | string |  |
| `dueAmount` | number |  |
| `dueDate` | string |  |
| `eBillCreated` | boolean |  |
| `entity` | string |  |
| `exchangeRate` | object |  |
| `expense.count` | number |  |
| `expense.totalAmount` | number |  |
| `fullPaymentDate` | string |  |
| `glPostingDate` | string |  |
| `hasAmortizedLines` | boolean |  |
| `hasAutoPay` | boolean |  |
| `hasLinkedPurchaseOrders` | boolean |  |
| `id` | string |  |
| `invoiceDate` | string |  |
| `invoiceNumber` | string |  |
| `invoiceProductId` | string |  |
| `is1099MissingBill` | boolean |  |
| `isActive` | string |  |
| `isAutoSaved` | boolean |  |
| `isSppCreated` | boolean |  |
| `isVcardStpCandidate` | boolean |  |
| `item.count` | number |  |
| `item.totalAmount` | number |  |
| `lastPaymentDate` | string |  |
| `localAmount` | object |  |
| `locationId` | string |  |
| `multipleBillLineItems` | boolean |  |
| `numApprPolicyEx` | number |  |
| `organizationName` | string |  |
| `orgId` | string |  |
| `paidAmount` | number |  |
| `payFromBankAccountId` | string |  |
| `payFromChartOfAccountId` | string |  |
| `paymentStatus` | string |  |
| `paymentTermId` | string |  |
| `poNumber` | string |  |
| `quickbooksId` | object |  |
| `scheduledAmount` | number |  |
| `source` | string |  |
| `uiPaymentStatus` | string |  |
| `updatedTime` | string |  |
| `useBillDesc` | boolean |  |
| `vendorId` | string |  |

## Native endpoint

Through the native BILL Payables & Receivables API, this operation is `POST List/Bill.json` (base URL `https://api.bill.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bills.md) for the provider-specific parameters and requirements.

