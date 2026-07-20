# Create Sales Activity with Freshworks CRM

Creates a new sales activity in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sales_activities`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Sales Activity](https://developers.freshworks.com/crm/api/#create_sales_activity)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sales_activity` | body | `object` | yes |
| `sales_activity.end_date` | body | `string` | no |
| `sales_activity.notes` | body | `string` | no |
| `sales_activity.owner_id` | body | `number` | yes |
| `sales_activity.sales_activity_outcome_id` | body | `number` | no |
| `sales_activity.sales_activity_type_id` | body | `number` | yes |
| `sales_activity.start_date` | body | `string` | no |
| `sales_activity.targetable_id` | body | `number` | yes |
| `sales_activity.targetable_type` | body | `string` | yes |
| `sales_activity.title` | body | `string` | yes |
