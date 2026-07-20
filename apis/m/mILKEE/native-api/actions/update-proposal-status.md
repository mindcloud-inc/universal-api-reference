# Update Proposal Status with MILKEE

Updates a proposal status in MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/proposals/:proposalId/mark-as`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Update Proposal Status](https://apidocs.milkee.ch/api/resources/proposals.html#status-andern-mark-as)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `proposal_id` | path | `string` | yes | The numeric MILKEE proposal ID used in the request path. |
| `status` | query | `string` | yes | Target proposal status transition. |
