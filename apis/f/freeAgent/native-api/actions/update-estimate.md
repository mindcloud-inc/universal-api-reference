# Update Estimate with FreeAgent

Updates an existing estimate in FreeAgent.

## Endpoint

- **Method:** `PUT`
- **Path:** `/estimates/:id`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Update Estimate](https://dev.freeagent.com/docs/estimates#update-an-estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | FreeAgent estimate ID. |
| `estimate` | body | `object` | no | Estimate payload. |
| `estimate.status` | body | `string` | no | Estimate status. |
| `estimate.estimate_type` | body | `string` | no | Estimate type. |
| `estimate.contact` | body | `string` | no | Contact for whom the estimate is created. |
| `estimate.project` | body | `string` | no | Project being estimated. |
| `estimate.reference` | body | `string` | no | Free-text reference. |
| `estimate.dated_on` | body | `date` | no | Date of estimate in YYYY-MM-DD format. |
| `estimate.currency` | body | `string` | no | Estimate currency. |
| `estimate.notes` | body | `string` | no | Additional text. |
