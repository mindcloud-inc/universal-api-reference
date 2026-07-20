# Create Invoice with Vtiger CRM

Creates a new invoice in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=Invoice`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Invoice](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON string for an Invoice payload. Include `subject`, `assigned_user_id`, `bill_street`, `ship_street`, and numbered line-item keys like `hdnProductId1`, `productName1`, `qty1`, `listPrice1`, `totalProductCount`. |
