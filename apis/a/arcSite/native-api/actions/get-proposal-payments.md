# Get Proposal Payments with ArcSite

Retrieves received payments for a specific ArcSite proposal.

## Endpoint

- **Method:** `GET`
- **Path:** `/proposals/:proposalId/payments`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Get Proposal Payments](https://dev.arcsite.com/#get-proposal-payments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `proposalId` | path | `string` | yes | The ID of the proposal. |
