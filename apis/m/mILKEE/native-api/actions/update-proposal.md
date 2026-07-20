# Update Proposal with MILKEE

Updates an existing proposal in MILKEE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:companyId/proposals/:proposalId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Update Proposal](https://apidocs.milkee.ch/api/resources/proposals.html#offerte-aktualisieren)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `customer_id` | body | `number` | no | Customer ID for the proposal. |
| `discount_rate` | body | `number` | no | Overall discount percentage. |
| `positions` | body | `string` | no | Proposal positions as a JSON string. |
| `project_id` | body | `number` | no | Associated project ID. |
| `proposal_id` | path | `string` | yes | The numeric MILKEE proposal ID used in the request path. |
| `remarks` | body | `string` | no | Bottom remarks. |
| `signature_remark` | body | `string` | no | Text shown in the signature area. |
| `tax_rate_id` | body | `number` | no | Tax rate ID. |
| `title` | body | `string` | no | Proposal title. |
| `valid_until` | body | `string` | no | Proposal expiration date. |
| `with_signature` | body | `boolean` | no | Show a signature area on the proposal. |
