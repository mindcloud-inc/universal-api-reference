# List Project Allocations with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/Allocations`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Project Allocations](https://developers.gobridgit.com/reference/allocations_query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The Project ID |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `personstate` | query | `list<string>` | no | State of persons to filter results by (Default Active) Accepted values: `Active`, `All`, `Deactivated`. |
| `daysUntilTimeOff` | query | `number` | no | Used to calculate the upcoming TimeOff unavailabilities based on the relativeDate |
| `type` | query | `list<string>` | no | Salaried role type to filter results by (Default to Operations) Accepted values: `All`, `Operations`, `Preconstruction`. |
