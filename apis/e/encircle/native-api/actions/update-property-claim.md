# Update Property Claim with Encircle

Updates a property claim in Encircle.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/property_claims/:property_claim_id`
- **Base URL:** `https://api.encircleapp.com`
- **Official documentation:** [Update Property Claim](https://encircleinc.github.io/public-api/#/paths/~1v1~1property_claims~1{property_claim_id}/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property_claim_id` | path | `number` | yes | — |
| `type_of_loss` | body | `string` | no | — |
| `locale` | body | `list` | no | Accepted values: `en`, `es`, `fr`. |
| `adjuster_name` | body | `string` | no | — |
| `assignment_identifier` | body | `string` | no | — |
| `cat_code` | body | `string` | no | — |
| `contents_estimate` | body | `number` | no | — |
| `contractor_identifier` | body | `string` | no | — |
| `date_claim_created` | body | `date` | no | — |
| `date_of_loss` | body | `date` | no | — |
| `default_depreciation` | body | `number` | no | — |
| `emergency_estimate` | body | `number` | no | — |
| `full_address` | body | `string` | no | — |
| `insurer_identifier` | body | `string` | no | — |
| `loss_details` | body | `string` | no | — |
| `max_depreciation` | body | `number` | no | — |
| `policyholder_email_address` | body | `string` | no | — |
| `policyholder_name` | body | `string` | no | — |
| `policyholder_phone_number` | body | `string` | no | — |
| `project_manager_name` | body | `string` | no | — |
| `repair_estimate` | body | `number` | no | — |
| `sales_tax` | body | `number` | no | — |
| `broker_or_agent_name` | body | `string` | no | — |
| `insurance_company_name` | body | `string` | no | — |
| `policy_number` | body | `string` | no | — |
