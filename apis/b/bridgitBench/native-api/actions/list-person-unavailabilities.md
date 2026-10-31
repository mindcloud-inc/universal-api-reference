# List Person Unavailabilities with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:id/unavailabilities`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Person Unavailabilities](https://developers.gobridgit.com/reference/personunavailabilities_getunavailabilities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the person to get unavailabilities for |
| `start` | query | `date` | no | Date from which to start the range (Default: 0001-01-01) |
| `end` | query | `date` | no | Date from which to end the range (Default: 9999-12-31) |
| `sortOrder` | query | `list<string>` | no | The order to return unavailabilities. Default is StartDateAscending Accepted values: `EndDateDescending`, `StartDateAscending`. |
