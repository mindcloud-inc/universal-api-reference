# List Verification Results with Wbiztool

Retrieves verification results for a campaign in Wbiztool.

## Endpoint

- **Method:** `GET`
- **Path:** `/verification/results/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [List Verification Results](https://wbiztool.com/docs/verification-results-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | query | `number` | yes | Verification campaign ID to list results for. |
| `status` | query | `string` | no | Optional result status filter. |
| `limit` | query | `number` | no | Maximum number of results to return. |
| `offset` | query | `string` | no | Result offset for pagination. Pass numeric text such as 0, 25, or 50. |
