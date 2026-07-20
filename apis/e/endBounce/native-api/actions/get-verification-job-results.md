# Get Verification Job Results with EndBounce

Retrieves verification job results from EndBounce.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/jobs/:request_id/results`
- **Base URL:** `https://api.endbounce.com/api/integrations`
- **Official documentation:** [Get Verification Job Results](https://app.endbounce.com/integrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Verification job request ID. |
| `status` | query | `string` | no | Filter results by verification status. |
| `offset` | query | `number` | no | Row offset for paginating job results. |
| `limit` | query | `number` | no | Maximum number of result rows to return. |
