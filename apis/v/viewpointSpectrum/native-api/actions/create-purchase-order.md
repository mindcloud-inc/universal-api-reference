# Create Purchase Order with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `purchaseOrders`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Create Purchase Order](https://help.trimble.com/doc/spectrum/spectrum/api-web-services/list-of-web-services/purchase-order-services/purchase-order-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrders[]` | body | `array<object>` | yes | Purchase order batch items. |
| `purchaseOrders[].Company_Code` | body | `string` | yes | Company code. Required; must be a valid company. |
| `purchaseOrders[].PO_Number` | body | `string` | yes | Purchase order number. Required; leave blank to auto-assign the next PO number. |
| `purchaseOrders[].Vendor_Code` | body | `string` | yes | Vendor code. Required; valid vendor code must exist in the company. |
| `purchaseOrders[].Warehouse_Code` | body | `string` | no | Warehouse code. Required unless no non-direct cost detail records are included. |
| `purchaseOrders[].Job_Number` | body | `string` | no | Job number. Required unless a valid warehouse code is defined and there are no direct job cost detail records. |
| `purchaseOrders[].VAT_Code` | body | `string` | no | VAT code. Must exist in the company when used. |
| `purchaseOrders[].Status_Flag` | body | `string` | no | PO status. P = Proposed, O = Open, C = Closed. Blank defaults to Proposed. |
| `purchaseOrders[].Cost_Center` | body | `string` | no | Cost center code. Must be valid if cost centers are enabled. |
| `purchaseOrders[].Remarks` | body | `string` | no | Remarks code or free text, up to 29 characters. |
| `purchaseOrders[].Special_Instructions` | body | `string` | no | Special instructions code or free text, up to 29 characters. |
| `purchaseOrders[].Ship_To_Code` | body | `string` | no | Ship-to code. D = Default, J = Job, I = Input. Blank defaults to D. |
| `purchaseOrders[].Ship_Name` | body | `string` | no | Ship-to name. Required when ship-to code is I. |
| `purchaseOrders[].Ship_Address_1` | body | `string` | no | Ship-to address line 1. Required when ship-to code is I. |
| `purchaseOrders[].Ship_Address_2` | body | `string` | no | Ship-to address line 2. |
| `purchaseOrders[].Ship_City` | body | `string` | no | Ship-to city. Required when ship-to code is I. |
| `purchaseOrders[].Ship_State` | body | `string` | no | Ship-to state. Required when ship-to code is I. |
| `purchaseOrders[].Ship_Zip_Code` | body | `string` | no | Ship-to postal code. Required when ship-to code is I. |
| `purchaseOrders[].Ship_Via` | body | `string` | no | Ship via code or free text. Blank defaults from Purchase Order Installation. |
| `purchaseOrders[].Ship_Terms` | body | `string` | no | Shipping terms code or free text. Blank defaults from Purchase Order Installation. |
| `purchaseOrders[].FOB` | body | `string` | no | FOB text. Blank defaults from Purchase Order Installation. |
| `purchaseOrders[].Ordered_By` | body | `string` | no | Ordered by, up to 20 characters. |
| `purchaseOrders[].Confirmed_By` | body | `string` | no | Confirmed by. Blank defaults from Purchase Order Installation. |
| `purchaseOrders[].PO_Order_Date` | body | `date` | no | Order date in MM/DD/CCYY format. Blank defaults to the current PO processing date. |
| `purchaseOrders[].Batch_Code` | body | `string` | no | Batch code. Blank defaults to the operator code from Authorization_ID. |
| `purchaseOrders[].Terms_Code` | body | `string` | no | Payment terms basis. A = Based on invoice date, B = Based on first of next month. |
| `purchaseOrders[].Payment_Days` | body | `number` | no | Payment number of days. Must be non-negative. |
| `purchaseOrders[].Discount_From_Code` | body | `string` | no | Discount due basis. A = Based on invoice date, B = Based on first of next month. |
| `purchaseOrders[].Discount_Days` | body | `number` | no | Discount number of days. Must be non-negative. |
| `purchaseOrders[].Terms_Percent` | body | `number` | no | Discount percent. Enter 12.34 for 12.34%; must be non-negative. |
| `purchaseOrders[].Terms_Description` | body | `string` | no | Terms description, up to 20 characters. Constructed automatically when blank. |
| `purchaseOrders[].Resale_Flag` | body | `string` | no | For resale flag. Y = For resale, N = Not for resale. |
| `purchaseOrders[].Tax_Code` | body | `string` | no | Default sales/use tax code. Must exist in the company when used. |
| `purchaseOrders[].Routing_Code` | body | `string` | no | Routing code. Must exist in the company when used. |
| `purchaseOrders[].PO_Delivery_Date` | body | `date` | no | Delivery date in MM/DD/CCYY format. |
| `purchaseOrders[].PO_Method` | body | `string` | no | Receiving method. Must be 1 or 2 when supplied. |
| `purchaseOrders[].PO_Type` | body | `string` | no | Pricing type. U = Unit price, L = Lump sum. |
| `purchaseOrders[].Bank_Account_Code` | body | `string` | no | Credit card account code. Must be a credit-card type account when used. |
| `purchaseOrders[].Card_Number` | body | `string` | no | Card number. Required if the account tracks card numbers. |
| `purchaseOrders[].Comment` | body | `string` | no | Header comment, up to 250 characters. |
| `purchaseOrders[].poDetails[]` | body | `array<object>` | no | Purchase order detail lines. |
| `purchaseOrders[].poDetails[].Detail_Entry_Type` | body | `string` | no | Detail entry type. D = Defined item code, N = Non-stock item, M = Message-only. |
| `purchaseOrders[].poDetails[].PO_Quantity` | body | `number` | no | Quantity. Required and non-zero unless this is a message-only line. |
| `purchaseOrders[].poDetails[].Item_ID` | body | `string` | no | Item ID. Required unless this is a message-only line. |
| `purchaseOrders[].poDetails[].Item_Description` | body | `string` | no | Item description. Used for non-stock items; stock item descriptions default from inventory item master. |
| `purchaseOrders[].poDetails[].Unit_Of_Measure` | body | `string` | no | Unit of measure, up to 3 characters. |
| `purchaseOrders[].poDetails[].Item_Price` | body | `number` | no | Item price. Blank defaults using Spectrum purchase order rules. |
| `purchaseOrders[].poDetails[].Item_Discount_Percent` | body | `number` | no | Line discount percent. Enter 12.34 for 12.34%; must be non-negative. |
| `purchaseOrders[].poDetails[].GL_Account` | body | `string` | no | G/L account. Required unless this is a message-only line. |
| `purchaseOrders[].poDetails[].Phase_Code` | body | `string` | no | Phase code. Required unless this is a message-only line or non-job purchase. |
| `purchaseOrders[].poDetails[].Cost_Type` | body | `string` | no | Cost type. Required unless this is a message-only line or non-job purchase. |
| `purchaseOrders[].poDetails[].Tax_Code` | body | `string` | no | Detail sales/use tax code. Must exist in the company when used. |
| `purchaseOrders[].poDetails[].Delivery_Date` | body | `date` | no | Detail delivery date in MM/DD/CCYY format. |
| `purchaseOrders[].poDetails[].Message` | body | `string` | no | Message text. Required for message-only lines; up to 250 characters. |
| `purchaseOrders[].poDetails[].Cost_Center` | body | `string` | no | Detail cost center. Must be valid if cost centers are enabled. |
