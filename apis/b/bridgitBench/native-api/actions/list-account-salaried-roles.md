# List Account Salaried Roles with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/Accounts/:id/roles`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Account Salaried Roles](https://developers.gobridgit.com/reference/accounts_queryroles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Account ID |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `unfilled` | query | `boolean` | no | If true, limits the results to include only roles that are unfilled; that is, they don't have any allocations. If false, the results include all roles in the account, both filled and unfilled. |
| `projectId` | query | `number` | no | (Optional) Filter role(s) for specified project ID |
| `filledState` | query | `list<number>` | no | (Optional) Filters the result by the filled state of the roles Accepted values: `0`, `1`, `2`. |
| `roleIds` | query | `number` | no | (Optional) Filters the result to contain roles that match the ids passed in. Works as an AND with filledState and roleNameIds Send multiple values as a array. |
| `roleNameIds` | query | `number` | no | (Optional) Filters the result to contain roles that match the ids passed in. Works as an AND with filledState and roleIds Send multiple values as a array. |
| `projectState` | query | `list<string>` | no | (Optional) Filters the result by the state of the project the role is on Accepted values: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. |
| `roleState` | query | `list<string>` | no | (Optional) Filters the result by the state of the role dates: Current, Upcoming, Past, or All Accepted values: `All`, `Current`, `Past`, `Upcoming`. |
| `type` | query | `list<string>` | no | (Optional)Salaried role type to filter results by (Defaults to Operations) Accepted values: `All`, `Operations`, `Preconstruction`. |
