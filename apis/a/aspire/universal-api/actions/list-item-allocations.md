# Aspire: List Item Allocations



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-item-allocations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-item-allocations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-item-allocations?${params}`, {
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
      "acceptedDateTime": "string",
      "acceptedUserID": 1,
      "acceptedUserName": "Ava Chen",
      "accountingPeriodYear": {},
      "allocationStatus": "string",
      "branchID": 1,
      "catalogItemID": 1,
      "catalogItemName": "Ava Chen",
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "deviceID": {},
      "deviceName": {},
      "ePAName": {},
      "ePANumber": {},
      "fromWorkTicketIDToInventory": {},
      "inventoryAdjustment": true,
      "inventoryLocationID": {},
      "inventoryLocationName": {},
      "invoiceID": 1,
      "itemAllocationDate": "string",
      "itemAllocationID": 1,
      "itemName": "Ava Chen",
      "itemQuantity": 1,
      "itemTotalCost": 1,
      "itemType": "string",
      "itemUnitCost": 1,
      "jobInventoryItemAllocationID": {},
      "lastModifiedByUserID": 1,
      "lastModifiedByUserName": "Ava Chen",
      "lastModifiedDateTime": "string",
      "preReceivedItemQuantity": 1,
      "receiptID": 1,
      "receiptItemID": 1,
      "subcontractorAcceptedDateTime": {},
      "subcontractorAcceptedUserID": {},
      "subcontractorCreated": true,
      "subcontractorRouteID": {},
      "subcontractorServicesRenderedDate": {},
      "transactionID": {},
      "vendorInvoiceNumber": "string",
      "workTicketID": 1,
      "workTicketNumber": 1,
      "workTicketTimeID": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedDateTime` | string |  |
| `acceptedUserID` | number |  |
| `acceptedUserName` | string |  |
| `accountingPeriodYear` | object |  |
| `allocationStatus` | string |  |
| `branchID` | number |  |
| `catalogItemID` | number |  |
| `catalogItemName` | string |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `deviceID` | object |  |
| `deviceName` | object |  |
| `ePAName` | object |  |
| `ePANumber` | object |  |
| `fromWorkTicketIDToInventory` | object |  |
| `inventoryAdjustment` | boolean |  |
| `inventoryLocationID` | object |  |
| `inventoryLocationName` | object |  |
| `invoiceID` | number |  |
| `itemAllocationDate` | string |  |
| `itemAllocationID` | number |  |
| `itemName` | string |  |
| `itemQuantity` | number |  |
| `itemTotalCost` | number |  |
| `itemType` | string |  |
| `itemUnitCost` | number |  |
| `jobInventoryItemAllocationID` | object |  |
| `lastModifiedByUserID` | number |  |
| `lastModifiedByUserName` | string |  |
| `lastModifiedDateTime` | string |  |
| `preReceivedItemQuantity` | number |  |
| `receiptID` | number |  |
| `receiptItemID` | number |  |
| `subcontractorAcceptedDateTime` | object |  |
| `subcontractorAcceptedUserID` | object |  |
| `subcontractorCreated` | boolean |  |
| `subcontractorRouteID` | object |  |
| `subcontractorServicesRenderedDate` | object |  |
| `transactionID` | object |  |
| `vendorInvoiceNumber` | string |  |
| `workTicketID` | number |  |
| `workTicketNumber` | number |  |
| `workTicketTimeID` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `GET ItemAllocations` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-item-allocations.md) for the provider-specific parameters and requirements.

