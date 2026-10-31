# Get Person Historical Experience with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Get Person Historical Experience](https://developers.gobridgit.com/reference/personhistoricalexperiences_getone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID. |
| `personId` | path | `number` | yes | The person ID. |
| `historicalExperienceId` | path | `string` | yes | The historical experience ID. |
