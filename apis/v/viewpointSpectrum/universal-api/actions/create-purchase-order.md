# Viewpoint Spectrum: Create Purchase Order



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrders[]": [
    {}
  ],
  "purchaseOrders[].Company_Code": "string",
  "purchaseOrders[].PO_Number": "string",
  "purchaseOrders[].Vendor_Code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaseOrders[]": [{}],
    "purchaseOrders[].Company_Code": "string",
    "purchaseOrders[].PO_Number": "string",
    "purchaseOrders[].Vendor_Code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrders[]` | array<object> | yes | Purchase order batch items. |
| `purchaseOrders[].Company_Code` | string | yes | Company code. Required; must be a valid company. |
| `purchaseOrders[].PO_Number` | string | yes | Purchase order number. Required; leave blank to auto-assign the next PO number. |
| `purchaseOrders[].Vendor_Code` | string | yes | Vendor code. Required; valid vendor code must exist in the company. |
| `purchaseOrders[].Warehouse_Code` | string | no | Warehouse code. Required unless no non-direct cost detail records are included. |
| `purchaseOrders[].Job_Number` | string | no | Job number. Required unless a valid warehouse code is defined and there are no direct job cost detail records. |
| `purchaseOrders[].VAT_Code` | string | no | VAT code. Must exist in the company when used. |
| `purchaseOrders[].Status_Flag` | string | no | PO status. P = Proposed, O = Open, C = Closed. Blank defaults to Proposed. |
| `purchaseOrders[].Cost_Center` | string | no | Cost center code. Must be valid if cost centers are enabled. |
| `purchaseOrders[].Remarks` | string | no | Remarks code or free text, up to 29 characters. |
| `purchaseOrders[].Special_Instructions` | string | no | Special instructions code or free text, up to 29 characters. |
| `purchaseOrders[].Ship_To_Code` | string | no | Ship-to code. D = Default, J = Job, I = Input. Blank defaults to D. |
| `purchaseOrders[].Ship_Name` | string | no | Ship-to name. Required when ship-to code is I. |
| `purchaseOrders[].Ship_Address_1` | string | no | Ship-to address line 1. Required when ship-to code is I. |
| `purchaseOrders[].Ship_Address_2` | string | no | Ship-to address line 2. |
| `purchaseOrders[].Ship_City` | string | no | Ship-to city. Required when ship-to code is I. |
| `purchaseOrders[].Ship_State` | string | no | Ship-to state. Required when ship-to code is I. |
| `purchaseOrders[].Ship_Zip_Code` | string | no | Ship-to postal code. Required when ship-to code is I. |
| `purchaseOrders[].Ship_Via` | string | no | Ship via code or free text. Blank defaults from Purchase Order Installation. |
| `purchaseOrders[].Ship_Terms` | string | no | Shipping terms code or free text. Blank defaults from Purchase Order Installation. |
| `purchaseOrders[].FOB` | string | no | FOB text. Blank defaults from Purchase Order Installation. |
| `purchaseOrders[].Ordered_By` | string | no | Ordered by, up to 20 characters. |
| `purchaseOrders[].Confirmed_By` | string | no | Confirmed by. Blank defaults from Purchase Order Installation. |
| `purchaseOrders[].PO_Order_Date` | date | no | Order date in MM/DD/CCYY format. Blank defaults to the current PO processing date. |
| `purchaseOrders[].Batch_Code` | string | no | Batch code. Blank defaults to the operator code from Authorization_ID. |
| `purchaseOrders[].Terms_Code` | string | no | Payment terms basis. A = Based on invoice date, B = Based on first of next month. |
| `purchaseOrders[].Payment_Days` | number | no | Payment number of days. Must be non-negative. |
| `purchaseOrders[].Discount_From_Code` | string | no | Discount due basis. A = Based on invoice date, B = Based on first of next month. |
| `purchaseOrders[].Discount_Days` | number | no | Discount number of days. Must be non-negative. |
| `purchaseOrders[].Terms_Percent` | number | no | Discount percent. Enter 12.34 for 12.34%; must be non-negative. |
| `purchaseOrders[].Terms_Description` | string | no | Terms description, up to 20 characters. Constructed automatically when blank. |
| `purchaseOrders[].Resale_Flag` | string | no | For resale flag. Y = For resale, N = Not for resale. |
| `purchaseOrders[].Tax_Code` | string | no | Default sales/use tax code. Must exist in the company when used. |
| `purchaseOrders[].Routing_Code` | string | no | Routing code. Must exist in the company when used. |
| `purchaseOrders[].PO_Delivery_Date` | date | no | Delivery date in MM/DD/CCYY format. |
| `purchaseOrders[].PO_Method` | string | no | Receiving method. Must be 1 or 2 when supplied. |
| `purchaseOrders[].PO_Type` | string | no | Pricing type. U = Unit price, L = Lump sum. |
| `purchaseOrders[].Bank_Account_Code` | string | no | Credit card account code. Must be a credit-card type account when used. |
| `purchaseOrders[].Card_Number` | string | no | Card number. Required if the account tracks card numbers. |
| `purchaseOrders[].Comment` | string | no | Header comment, up to 250 characters. |
| `purchaseOrders[].poDetails[]` | array<object> | no | Purchase order detail lines. |
| `purchaseOrders[].poDetails[].Detail_Entry_Type` | string | no | Detail entry type. D = Defined item code, N = Non-stock item, M = Message-only. |
| `purchaseOrders[].poDetails[].PO_Quantity` | number | no | Quantity. Required and non-zero unless this is a message-only line. |
| `purchaseOrders[].poDetails[].Item_ID` | string | no | Item ID. Required unless this is a message-only line. |
| `purchaseOrders[].poDetails[].Item_Description` | string | no | Item description. Used for non-stock items; stock item descriptions default from inventory item master. |
| `purchaseOrders[].poDetails[].Unit_Of_Measure` | string | no | Unit of measure, up to 3 characters. |
| `purchaseOrders[].poDetails[].Item_Price` | number | no | Item price. Blank defaults using Spectrum purchase order rules. |
| `purchaseOrders[].poDetails[].Item_Discount_Percent` | number | no | Line discount percent. Enter 12.34 for 12.34%; must be non-negative. |
| `purchaseOrders[].poDetails[].GL_Account` | string | no | G/L account. Required unless this is a message-only line. |
| `purchaseOrders[].poDetails[].Phase_Code` | string | no | Phase code. Required unless this is a message-only line or non-job purchase. |
| `purchaseOrders[].poDetails[].Cost_Type` | string | no | Cost type. Required unless this is a message-only line or non-job purchase. |
| `purchaseOrders[].poDetails[].Tax_Code` | string | no | Detail sales/use tax code. Must exist in the company when used. |
| `purchaseOrders[].poDetails[].Delivery_Date` | date | no | Detail delivery date in MM/DD/CCYY format. |
| `purchaseOrders[].poDetails[].Message` | string | no | Message text. Required for message-only lines; up to 250 characters. |
| `purchaseOrders[].poDetails[].Cost_Center` | string | no | Detail cost center. Must be valid if cost centers are enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST purchaseOrders` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.

