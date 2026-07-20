# Create Record with Vtiger CRM

Creates a new record in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Record](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `elementType` | query | `string` | yes | Vtiger module name to create the record in. |
| `element` | query | `string` | yes | JSON object string for the record fields to create. |
