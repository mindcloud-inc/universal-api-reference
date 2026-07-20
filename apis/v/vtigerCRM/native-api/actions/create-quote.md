# Create Quote with Vtiger CRM

Creates a new quote in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=Quotes`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Quote](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON string for a Quote payload. Include `subject`, `quotestage`, `assigned_user_id`, `bill_street`, `ship_street`, and numbered line-item keys like `hdnProductId1`, `productName1`, `qty1`, `listPrice1`, `totalProductCount`. |
