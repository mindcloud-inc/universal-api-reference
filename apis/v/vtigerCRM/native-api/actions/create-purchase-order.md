# Create Purchase Order with Vtiger CRM

Creates a new purchase order in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=PurchaseOrder`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Purchase Order](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON string for a Purchase Order payload. Include `subject`, `vendor_id`, `postatus`, `assigned_user_id`, `bill_street`, `ship_street`, and numbered line-item keys like `hdnProductId1`, `productName1`, `qty1`, `listPrice1`, `totalProductCount`. |
