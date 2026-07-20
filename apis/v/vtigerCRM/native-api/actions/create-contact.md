# Create Contact with Vtiger CRM

Creates a new contact in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/create?elementType=Contacts`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Contact](https://vtap.vtiger.com/platform/rest-apis.html#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | body | `string` | yes | JSON object string for the Contact fields to create. |
