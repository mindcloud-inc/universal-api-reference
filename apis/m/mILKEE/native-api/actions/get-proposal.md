# Get Proposal with MILKEE

Retrieves a proposal from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/proposals/:proposalId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Get Proposal](https://apidocs.milkee.ch/api/resources/proposals.html#einzelne-offerte-abrufen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `proposal_id` | path | `string` | yes | The numeric MILKEE proposal ID used in the request path. |
