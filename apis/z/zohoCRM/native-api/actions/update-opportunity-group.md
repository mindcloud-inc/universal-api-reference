# Update Opportunity Group with Zoho CRM

## Endpoint

- **Method:** `PUT`
- **Path:** `/Opportunity_Groups`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Update Opportunity Group](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Zoho CRM Opportunity Group record ID to update. |
| `Name` | body | `string` | no | Opportunity Group name. |
| `dealId` | body | `string` | no | Zoho CRM Deal record ID to associate with the Opportunity Group. |
| `Total_Price` | body | `number` | no | Opportunity Group total price value. |
| `Description` | body | `string` | no | Opportunity Group description. |
