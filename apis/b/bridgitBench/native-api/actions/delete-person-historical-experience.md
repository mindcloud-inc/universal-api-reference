# Delete Person Historical Experience with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Historical Experience](https://developers.gobridgit.com/reference/personhistoricalexperiences_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID. |
| `personId` | path | `number` | yes | The person ID. |
| `historicalExperienceId` | path | `string` | yes | The historical experience ID. |
