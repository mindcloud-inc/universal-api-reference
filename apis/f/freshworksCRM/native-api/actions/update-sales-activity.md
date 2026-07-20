# Update Sales Activity with Freshworks CRM

Updates an existing sales activity in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/sales_activities/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Sales Activity](https://developers.freshworks.com/crm/api/#update_a_sales_activity)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `sales_activity` | body | `object` | yes |
| `sales_activity.notes` | body | `string` | no |
| `sales_activity.owner_id` | body | `number` | no |
| `sales_activity.targetable_id` | body | `number` | no |
| `sales_activity.targetable_type` | body | `string` | no |
| `sales_activity.title` | body | `string` | no |
