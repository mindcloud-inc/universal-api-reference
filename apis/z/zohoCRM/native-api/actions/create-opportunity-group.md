# Create Opportunity Group with Zoho CRM

Creates a new Opportunity Group in Zoho CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Opportunity_Groups`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Create Opportunity Group](https://www.zoho.com/crm/developer/docs/api/v8/insert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Opportunity Group name. |
| `dealId` | body | `string` | yes | Zoho CRM Deal record ID to associate with the Opportunity Group. |
| `totalPrice` | body | `number` | yes | Opportunity Group total price value. |
| `description` | body | `string` | no | Opportunity Group description. |
