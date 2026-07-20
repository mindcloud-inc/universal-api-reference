# Create Deal with Vtiger CRM

Creates a new deal in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=Potentials`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Deal](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON object string for the Deal fields to create. |
