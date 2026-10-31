# List Projects with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/Projects`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Projects](https://developers.gobridgit.com/reference/projects_query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `name` | query | `string` | no | Name filter that affects whether or not to return projects back with/without the name contains partial match (Default: Empty) |
| `issues` | query | `list<number>` | no | State filter that affects whether or not to return projects back with/without or any issues (Default: All) Accepted values: `0`, `1`, `2`. |
| `ids` | query | `number` | no | Optional comma delimited list of project IDs to filter the result on Send multiple values as a string separated by `,`. |
| `projectState` | query | `list<string>` | no | Optional comma delimited list for filtering results by project state. Accepted values: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. Send multiple values as a string separated by `,`. |
| `includeProjectNumber` | query | `boolean` | no | Whether to include the Project Number field in the response (Default: false) |
