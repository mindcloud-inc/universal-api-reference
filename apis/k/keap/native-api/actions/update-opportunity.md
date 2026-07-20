# Update Opportunity with Keap

## Endpoint

- **Method:** `PATCH`
- **Path:** `/opportunities/{opportunity_id}`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Update Opportunity](https://developer.keap.com/docs/restv2/#tag/Opportunity/operation/updateOpportunity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | body | `string` | no | — |
| `contact_id` | body | `string` | no | — |
| `custom_fields` | body | `string` | no | — |
| `estimated_close_time` | body | `string` | no | — |
| `include_in_forecast` | body | `string` | no | — |
| `next_action_notes` | body | `string` | no | — |
| `next_action_time` | body | `string` | no | — |
| `opportunity_id` | path | `string` | yes | The unique identifier of the opportunity. |
| `opportunity_notes` | body | `string` | no | — |
| `opportunity_title` | body | `string` | no | — |
| `projected_revenue_high` | body | `string` | no | — |
| `projected_revenue_low` | body | `string` | no | — |
| `stage_id` | body | `string` | no | — |
| `update_mask` | query | `string` | no | — |
| `user_id` | body | `string` | no | — |
