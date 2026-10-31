# List Project Roles with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/roles`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Project Roles](https://developers.gobridgit.com/reference/projectroles_query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the role belongs to |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `roleState` | query | `list<string>` | no | (Optional) Filters the result by the state of the role dates: Current, Upcoming, Past, or All Accepted values: `All`, `Current`, `Past`, `Upcoming`. |
| `type` | query | `list<string>` | no | (Optional)Salaried role type to filter results by (Defaults to Operations) Accepted values: `All`, `Operations`, `Preconstruction`. |
