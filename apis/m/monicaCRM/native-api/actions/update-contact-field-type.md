# Update Contact Field Type with Monica CRM

Updates an existing contact field type in Monica CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contactfieldtypes/:contactFieldTypeId`
- **Base URL:** `https://app.monicahq.com/api`
- **Official documentation:** [Update Contact Field Type](https://www.monicahq.com/api/contactfieldtypes)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactFieldTypeId` | path | `string` | yes |
| `name` | body | `string` | yes |
