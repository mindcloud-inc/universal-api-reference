# Get Organization Stats with Shuffler

Retrieves organization stats from Shuffler.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/{orgId}/stats`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Get Organization Stats](https://shuffler.io/docs/API#get-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Org Id path parameter. |
| `top` | query | `string` | no | Optional top limit. |
