# Aspire: Create Receipt

Creates a new receipt in your Aspire account.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ReceiptItems[].receiptItemID": 1,
  "VendorID": "string",
  "ReceiptItems[].itemAllocations[].inventoryLocationID": 1,
  "ReceiptItems[].itemAllocations[].itemQuantity": 1,
  "ReceiptItems[].ItemName": "Ava Chen",
  "ReceiptItems[].ItemQuantity": 1,
  "ReceiptItems[].ItemUnitCost": 1,
  "ReceiptItems[].ItemType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-receipt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ReceiptItems[].receiptItemID": 1,
    "VendorID": "string",
    "ReceiptItems[].itemAllocations[].inventoryLocationID": 1,
    "ReceiptItems[].itemAllocations[].itemQuantity": 1,
    "ReceiptItems[].ItemName": "Ava Chen",
    "ReceiptItems[].ItemQuantity": 1,
    "ReceiptItems[].ItemUnitCost": 1,
    "ReceiptItems[].ItemType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ReceiptItems[].itemAllocations[].workTicketID` | list<number> | no | Item allocations require either a WorkTicketID or an InventoryLocationID, can't have both. |
| `ReceiptItems[].receiptItemID` | number | yes |  |
| `VendorID` | list<string> | yes |  |
| `ReceiptItems[].catalogItemID` | list<number> | no |  |
| `ReceiptItems[].itemAllocations[].inventoryLocationID` | list<number> | yes | Item allocations require either a WorkTicketID or an InventoryLocationID, can't have both. |
| `WorkTicketID` | list<number> | no |  |
| `ReceiptItems[].catalogItemCategoryID` | list<number> | no |  |
| `ReceiptNote` | string | no |  |
| `ReceiptItems[].itemAllocations[].itemQuantity` | number | yes |  |
| `ReceiptItems[].ItemName` | string | yes |  |
| `VendorInvoiceNum` | string | no |  |
| `ReceiptItems[].ItemQuantity` | number | yes |  |
| `VendorInvoiceDate` | string | no |  |
| `BranchID` | list | no |  |
| `ReceiptItems[].ItemUnitCost` | number | yes |  |
| `ReceiptItems[]` | array<object> | no | There has to be at least one receipt item |
| `ReceiptItems[].ItemType` | list<string> | yes |  |
| `inventoryLocationID` | list<number> | no | The ID of an inventory location. Required if no WorkTicketID is provided, to avoid the error: `At least one of WorkTicketID or InventoryLocationID is required.` |
| `ReceiptItems[].ItemEstUnitCost` | number | no |  |
| `ReceiptItems[].receiptItemPrice` | number | no |  |
| `ReceivedDate` | string | no |  |
| `ReceiptItems[].itemAllocations[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "receiptID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `receiptID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `POST Receipts` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-receipt.md) for the provider-specific parameters and requirements.

