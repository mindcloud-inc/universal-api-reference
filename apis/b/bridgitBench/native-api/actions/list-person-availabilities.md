# List Person Availabilities with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons/availabilities`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Person Availabilities](https://developers.gobridgit.com/reference/persons_querynextavailables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `relativeDate` | query | `date` | no | Optional paramater used to calculate date based properties. If not provided, it is set to today's date in UTC. |
| `start` | query | `date` | no | Start date to filter availabilities from (default today UTC) |
| `end` | query | `date` | no | End date to filter availabilities to (default 10 years from today UTC) |
| `boundRange` | query | `boolean` | no | Setting this value to true will truncate the dates returned to the specified start and end date paramters |
| `ids` | query | `number` | no | Optional paramater of comma delimited ids for filtering results based on the person IDs provided Send multiple values as a string separated by `,`. |
| `includeUnavailable` | query | `boolean` | no | If this is set to true it will return the availabilities and next available dates even if a person doesn't have a next availability. If the person does not have a "nextAvailableDate", then the "availableInDays" property will be -1 |
