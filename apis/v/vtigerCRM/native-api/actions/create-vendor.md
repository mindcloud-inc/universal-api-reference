# Create Vendor with Vtiger CRM

Creates a new vendor in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=Vendors`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Vendor](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON object string for the Vendor fields to create. |
