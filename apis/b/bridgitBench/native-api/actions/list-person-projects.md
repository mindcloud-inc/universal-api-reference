# List Person Projects with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons/:id/projects`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Person Projects](https://developers.gobridgit.com/reference/persons_getprojects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | The Person ID |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `projectState` | query | `list<string>` | no | Optional parameter for filtering results by project state. Accepted values: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. |
