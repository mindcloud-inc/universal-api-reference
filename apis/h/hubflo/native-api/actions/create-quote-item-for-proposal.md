# Create Quote Item for Proposal with Hubflo

Creates a quote item for a Hubflo proposal.

## Endpoint

- **Method:** `POST`
- **Path:** `/proposals/:proposal_id/line-items`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Create Quote Item for Proposal](https://hubflo.readme.io/reference/post_api-v2-proposals-proposal-id-line-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `proposal_id` | path | `string` | yes |
| `title` | body | `string` | yes |
| `quantity` | body | `number` | yes |
| `vat` | body | `number` | yes |
| `description` | body | `string` | no |
| `kind` | body | `string` | no |
| `unit_price_excluding_tax` | body | `string` | no |
| `unit_cost_excluding_tax` | body | `string` | no |
| `discount` | body | `number` | no |
