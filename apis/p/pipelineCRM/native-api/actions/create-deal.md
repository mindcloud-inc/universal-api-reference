# Create Deal with Pipeline CRM

Creates a new deal in Pipeline CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/deals`
- **Base URL:** `https://api.pipelinecrm.com/api/v3`
- **Official documentation:** [Create Deal](https://app.pipelinecrm.com/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliver_assignment_email` | query | `boolean` | no | Send an assignment email when the deal is assigned to another user. |
| `deal.name` | body | `string` | no | The name of the deal. |
| `deal.summary` | body | `string` | no | Explanatory or descriptive text about the deal. |
| `deal.user_id` | body | `number` | no | The ID of the user who owns this deal. |
| `deal.status` | body | `number` | no | The deal status ID for this deal. |
| `deal.expected_close_date` | body | `date` | no | The date the deal is expected to close by (YYYY-MM-DD). |
| `deal.value` | body | `number` | no | The deal's value in its currency. |
| `deal.primary_contact_id` | body | `number` | no | The primary contact person ID associated with this deal. |
| `deal.person_ids[]` | body | `array<number>` | no | Person record IDs associated with this deal. |
| `deal.company_id` | body | `number` | no | The company ID associated with this deal. |
| `deal.company_name` | body | `string` | no | Creates or associates a company with this deal by name. |
| `deal.probability` | body | `number` | no | Probability from 0-100 that the deal will close. |
| `deal.deal_stage_id` | body | `number` | no | The deal stage ID for this deal. |
| `deal.deal_loss_reason_id` | body | `number` | no | The deal loss reason ID for this deal. |
| `deal.deal_won_reason_id` | body | `number` | no | The deal won reason ID for this deal. |
| `deal.deal_source` | body | `number` | no | The lead source ID for this deal. |
| `deal.tag_ids[]` | body | `array<number>` | no | Tag IDs to set on this deal. |
| `todo_template_id` | body | `number` | no | The todo template ID to apply to this deal. |
| `todo_template_user_id` | body | `number` | no | The owner of tasks created from the todo template. |
