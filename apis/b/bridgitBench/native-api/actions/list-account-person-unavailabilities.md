# List Account Person Unavailabilities with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/unavailabilities`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Account Person Unavailabilities](https://developers.gobridgit.com/reference/personunavailabilities_query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `start` | query | `date` | no | Date from which to start the range (Default: 0001-01-01) |
| `end` | query | `date` | no | Date from which to end the range (Default: 9999-12-31) |
| `boundRange` | query | `boolean` | no | Setting this value to true will truncate the dates returned to the specified start and end date paramters |
| `type` | query | `list<string>` | no | Type of the unavailability date range (Default: Unavailability) Accepted values: `All`, `PostEmployment`, `PreEmployment`, `TimeOff`, `Unavailability`. |
| `state` | query | `list<string>` | no | State of persons to filter results by (Default: Active) Accepted values: `Active`, `All`, `Deactivated`. |
| `personIds` | query | `number` | no | Optional comma delimited list of person IDs to filter the results if set Send multiple values as a string separated by `,`. |
