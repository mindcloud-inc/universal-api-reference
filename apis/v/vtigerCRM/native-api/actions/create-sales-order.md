# Create Sales Order with Vtiger CRM

Creates a new sales order in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=SalesOrder`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Sales Order](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON string for a Sales Order payload. Include `subject`, `sostatus`, `assigned_user_id`, `bill_street`, `ship_street`, and numbered line-item keys like `hdnProductId1`, `productName1`, `qty1`, `listPrice1`, `totalProductCount`. |
