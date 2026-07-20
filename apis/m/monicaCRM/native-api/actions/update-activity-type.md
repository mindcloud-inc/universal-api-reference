# Update Activity Type with Monica CRM

Updates an existing activity type in Monica CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/activitytypes/:activityTypeId`
- **Base URL:** `https://app.monicahq.com/api`
- **Official documentation:** [Update Activity Type](https://www.monicahq.com/api/activitytypes)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activity_type_category_id` | body | `string` | yes |
| `activityTypeId` | path | `string` | yes |
| `name` | body | `string` | yes |
