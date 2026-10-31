# List Person Allocations with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons/:id/allocations`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Person Allocations](https://developers.gobridgit.com/reference/persons_getallocations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | The Person's ID |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `start` | query | `date` | no | Start date to filter allocations from |
| `end` | query | `date` | no | End date to filter allocations to |
| `roleId` | query | `number` | no | Optional parameter to get allocations for a specific role |
| `projectState` | query | `list<string>` | no | Optional parameter for filtering results by project state. Accepted values: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. |
| `type` | query | `list<string>` | no | Optional parameter Salaried role type to filter results by (Default to Operations) Accepted values: `All`, `Operations`, `Preconstruction`. |
