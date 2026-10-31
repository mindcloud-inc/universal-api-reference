# Delete Person Historical Experience Field with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId/experience-fields/:experienceFieldId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Historical Experience Field](https://developers.gobridgit.com/reference/personhistoricalexperiencefields_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID. |
| `personId` | path | `number` | yes | The person ID. |
| `historicalExperienceId` | path | `string` | yes | The historical experience ID. |
| `experienceFieldId` | path | `string` | yes | The experience field ID. |
