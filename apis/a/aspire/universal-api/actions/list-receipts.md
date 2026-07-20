# Aspire: List Receipts

Lists Aspire receipts using the available OData query parameters. Use this to find existing receipts and inspect fields such as status, invoice metadata, notes, received date, items, and costs. Aspire receipts cannot be updated after createReceipt; there is no updateReceipt endpoint or field-level patch action. The only post-create change path is approveReceipt, and it can add or change only the vendor invoice number and vendor invoice date. If the user wants to change any other field on an existing receipt, surface that constraint upfront and offer to recreate the receipt with the corrected values.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-receipts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-receipts?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountingVendorID": "string",
      "approvedByUserName": "Ava Chen",
      "approvedDate": "string",
      "approvedUserID": 1,
      "branchCode": "string",
      "branchID": 1,
      "branchName": "Ava Chen",
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "inventoryLocationID": {},
      "isPurchaseCredit": true,
      "jobInventory": true,
      "lastModifiedByUserID": 1,
      "lastModifiedByUserName": "Ava Chen",
      "lastModifiedDateTime": "string",
      "masterReceiptID": {},
      "opportunityID": 1,
      "opportunityNumber": 1,
      "purchaseAddressLocationName": "Ava Chen",
      "purchaseNumberWithBranchPrefix": "string",
      "receiptID": 1,
      "receiptItems": [
        {
          "catalogItemCategoryID": 1,
          "catalogItemID": 1,
          "catalogItemName": "Ava Chen",
          "itemAllocations": [
            {
              "catalogItemID": 1,
              "inventoryLocationID": {},
              "inventoryLocationName": {},
              "itemAllocationID": 1,
              "itemName": "Ava Chen",
              "itemQuantity": 1,
              "itemTotalCost": 1,
              "itemType": "string",
              "itemUnitCost": 1,
              "opportunityID": 1,
              "opportunityNumber": 1,
              "workTicketID": 1,
              "workTicketNumber": 1
            }
          ],
          "itemEstUnitCost": 1,
          "itemExtendedCost": 1,
          "itemName": "Ava Chen",
          "itemQuantity": 1,
          "itemType": "string",
          "itemUnitCost": 1,
          "receiptItemID": 1,
          "receivedQuantity": 1
        }
      ],
      "receiptNote": {},
      "receiptNumber": 1,
      "receiptStatusID": 1,
      "receiptStatusName": "Ava Chen",
      "receiptTotalCost": 1,
      "receivedByUserName": "Ava Chen",
      "receivedDate": "string",
      "receivedUserID": 1,
      "revisionNumber": {},
      "shippedToAddressID": 1,
      "syncDate": "string",
      "syncError": {},
      "vendorID": 1,
      "vendorInvoiceDate": "string",
      "vendorInvoiceNum": "string",
      "workTicketID": 1,
      "workTicketNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingVendorID` | string |  |
| `approvedByUserName` | string |  |
| `approvedDate` | string |  |
| `approvedUserID` | number |  |
| `branchCode` | string |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `inventoryLocationID` | object |  |
| `isPurchaseCredit` | boolean |  |
| `jobInventory` | boolean |  |
| `lastModifiedByUserID` | number |  |
| `lastModifiedByUserName` | string |  |
| `lastModifiedDateTime` | string |  |
| `masterReceiptID` | object |  |
| `opportunityID` | number |  |
| `opportunityNumber` | number |  |
| `purchaseAddressLocationName` | string |  |
| `purchaseNumberWithBranchPrefix` | string |  |
| `receiptID` | number |  |
| `receiptItems[].catalogItemCategoryID` | number |  |
| `receiptItems[].catalogItemID` | number |  |
| `receiptItems[].catalogItemName` | string |  |
| `receiptItems[].itemAllocations[].catalogItemID` | number |  |
| `receiptItems[].itemAllocations[].inventoryLocationID` | object |  |
| `receiptItems[].itemAllocations[].inventoryLocationName` | object |  |
| `receiptItems[].itemAllocations[].itemAllocationID` | number |  |
| `receiptItems[].itemAllocations[].itemName` | string |  |
| `receiptItems[].itemAllocations[].itemQuantity` | number |  |
| `receiptItems[].itemAllocations[].itemTotalCost` | number |  |
| `receiptItems[].itemAllocations[].itemType` | string |  |
| `receiptItems[].itemAllocations[].itemUnitCost` | number |  |
| `receiptItems[].itemAllocations[].opportunityID` | number |  |
| `receiptItems[].itemAllocations[].opportunityNumber` | number |  |
| `receiptItems[].itemAllocations[].workTicketID` | number |  |
| `receiptItems[].itemAllocations[].workTicketNumber` | number |  |
| `receiptItems[].itemEstUnitCost` | number |  |
| `receiptItems[].itemExtendedCost` | number |  |
| `receiptItems[].itemName` | string |  |
| `receiptItems[].itemQuantity` | number |  |
| `receiptItems[].itemType` | string |  |
| `receiptItems[].itemUnitCost` | number |  |
| `receiptItems[].receiptItemID` | number |  |
| `receiptItems[].receivedQuantity` | number |  |
| `receiptNote` | object |  |
| `receiptNumber` | number |  |
| `receiptStatusID` | number |  |
| `receiptStatusName` | string |  |
| `receiptTotalCost` | number |  |
| `receivedByUserName` | string |  |
| `receivedDate` | string |  |
| `receivedUserID` | number |  |
| `revisionNumber` | object |  |
| `shippedToAddressID` | number |  |
| `syncDate` | string |  |
| `syncError` | object |  |
| `vendorID` | number |  |
| `vendorInvoiceDate` | string |  |
| `vendorInvoiceNum` | string |  |
| `workTicketID` | number |  |
| `workTicketNumber` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Receipts` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-receipts.md) for the provider-specific parameters and requirements.

