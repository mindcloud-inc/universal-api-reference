# List Gates with Statsig

Retrieves gates from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/gates`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Gates](https://docs.statsig.com/api-reference/gates/list-gates)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idType` | query | `string` | no | Filter by idType |
| `type` | query | `string` | no | Filter by type |
| `typeReason` | query | `string` | no | Filter by typeReason |
| `passRate` | query | `string` | no | Filter by pass rate of the gates, as determined by a sampling of overall true/false values returned: 0, 100, or INBETWEEN (pass rate greater than zero but less than 100) |
| `rolloutRate` | query | `string` | no | Filter by rollout rate of the gates: 0 (all rules are set to pass 0%), 100 (all rules pass 100% including an "everyone" catch all rule), or INBETWEEN (at least one rule has a pass rate greater than 0 but less than 100) |
| `releasePipelineID` | query | `string` | no | Filter by release pipeline ID |
| `teamID` | query | `string` | no | Filter by team ID |
| `targetAppID` | query | `string` | no | Filter by target app ID |
| `includeArchived` | query | `string` | no | Include archived gates in the response |
| `store0100Exposures` | query | `string` | no | Filter gates by whether "Store 0/100 Exposures" is enabled. |
| `creatorName` | query | `string` | no | Name of the creator. |
| `creatorID` | query | `string` | no | ID of the user who created the entity. |
| `tags` | query | `string` | no | Filter by tags |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
