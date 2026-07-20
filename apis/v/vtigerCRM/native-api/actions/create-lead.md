# Create Lead with Vtiger CRM

Creates a new lead in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=Leads`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Lead](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON object string for the Lead fields to create. |
