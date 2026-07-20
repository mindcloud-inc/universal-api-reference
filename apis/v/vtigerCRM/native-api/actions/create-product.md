# Create Product with Vtiger CRM

Creates a new product in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=Products`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Product](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON object string for the Product fields to create. |
