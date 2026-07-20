# Create Estimate with FreeAgent

Creates a new estimate in FreeAgent.

## Endpoint

- **Method:** `POST`
- **Path:** `/estimates`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Create Estimate](https://dev.freeagent.com/docs/estimates#create-an-estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `estimate` | body | `object` | no | Estimate payload. |
| `estimate.status` | body | `string` | yes | Estimate status. |
| `estimate.estimate_type` | body | `string` | yes | Estimate type. |
| `estimate.contact` | body | `string` | yes | Contact for whom the estimate is created. |
| `estimate.project` | body | `string` | no | Project being estimated. |
| `estimate.reference` | body | `string` | yes | Free-text reference. |
| `estimate.dated_on` | body | `date` | yes | Date of estimate in YYYY-MM-DD format. |
| `estimate.currency` | body | `string` | yes | Estimate currency. |
| `estimate.notes` | body | `string` | no | Additional text. |
