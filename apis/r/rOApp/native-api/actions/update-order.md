# Update Order with RO App

## Endpoint

- **Method:** `PATCH`
- **Path:** `/orders/:order_id`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Update Order](https://roapp.readme.io/reference/update-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `number` | yes | Order ID |
| `branch_id` | body | `number` | no | Location ID |
| `order_type_id` | body | `number` | no | Estimate/Order Type ID |
| `manager_id` | body | `number` | no | Manager ID |
| `assignee_id` | body | `number` | no | Assigned Employee ID |
| `asset_id` | body | `number` | no | Asset ID |
| `client_id` | body | `number` | no | Client (Person / Organization) ID |
| `payer_id` | body | `number` | no | Payer (Person / Organization) ID |
| `ad_campaign_id` | body | `number` | no | Ad Campaign ID |
| `scheduled_for` | body | `date` | no | "Scheduled From" date and time (ISO 8601) |
| `scheduled_to` | body | `date` | no | "Scheduled To" date and time (ISO 8601) |
| `resource_id` | body | `number` | no | Resource ID |
| `malfunction` | body | `string` | no | Malfunction text |
| `manager_notes` | body | `string` | no | Manager notes |
| `engineer_notes` | body | `string` | no | Technician notes |
| `resume` | body | `string` | no | Conclusion / client recommendations |
| `estimated_price` | body | `string` | no | Estimates price or price range |
| `due_date` | body | `date` | no | Order Due Date (ISO 8601) |
| `urgent` | body | `string` | no | Is Order urgent? |
| `custom_fields` | body | `string` | no | Custom fields values in format {"f123": "value", "f234": "value"}, where "f123" and "f234" is a custom field id. |
