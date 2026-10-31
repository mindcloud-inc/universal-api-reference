# List Account Tasks with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/Accounts/:id/tasks`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Account Tasks](https://developers.gobridgit.com/reference/accounts_querytasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Account ID |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `projectIds` | query | `number` | no | (Optional) Filter task(s) to contain tasks that match the projectIds passed in. Send multiple values as a array. |
| `projectState` | query | `list<string>` | no | (Optional) Filters the result by the state of the project the role is on Accepted values: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. |
| `taskIds` | query | `string` | no | (Optional) Filters the result to contain tasks that match the taskIds passed in. Works as an AND with filledState and roleNameIds Send multiple values as a array. |
| `filledState` | query | `list<number>` | no | (Optional) Filters the result by the filled state of the roles Accepted values: `0`, `1`, `2`. |
| `roleIds` | query | `number` | no | (Optional) Filters the result to contain roles that match the ids passed in. Works as an AND with filledState and roleNameIds Send multiple values as a array. |
| `roleNameIds` | query | `number` | no | (Optional) Filters the result to contain roles that match the ids passed in. Works as an AND with filledState and roleIds Send multiple values as a array. |
| `roleState` | query | `list<string>` | no | (Optional) Filters the result by the state of the role dates: Current, Upcoming, Past, or All Accepted values: `All`, `Current`, `Past`, `Upcoming`. |
