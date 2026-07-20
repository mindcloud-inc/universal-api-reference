# Create Opportunity with Keap

## Endpoint

- **Method:** `POST`
- **Path:** `/opportunities`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Create Opportunity](https://developer.keap.com/docs/restv2/#tag/Opportunity/operation/createOpportunity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | body | `string` | no | Affiliate id |
| `contact_id` | body | `string` | no | Related contact id |
| `custom_fields` | body | `string` | no | — |
| `estimated_close_time` | body | `string` | no | — |
| `include_in_forecast` | body | `string` | no | — |
| `next_action_notes` | body | `string` | no | — |
| `next_action_time` | body | `string` | no | — |
| `opportunity_notes` | body | `string` | no | — |
| `opportunity_title` | body | `string` | yes | Opportunity title |
| `projected_revenue_high` | body | `string` | no | — |
| `projected_revenue_low` | body | `string` | no | — |
| `stage_id` | body | `string` | no | Opportunity stage id |
| `user_id` | body | `string` | no | — |
