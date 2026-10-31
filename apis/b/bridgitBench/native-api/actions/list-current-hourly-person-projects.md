# List Current Hourly Person Projects with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons/current-projects-hourly`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Current Hourly Person Projects](https://developers.gobridgit.com/reference/persons_getcurrentprojectshourly)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `personIds` | query | `number` | no | Optional paramater of comma delimited ids for filtering results based on the person IDs provided Send multiple values as a string separated by `,`. |
| `projectState` | query | `list<string>` | no | Optional parameter for filtering results by project state. Accepted values: `Active`, `All`, `Canceled`, `Complete`, `Lost`, `Pursuit`, `Upcoming`. |
