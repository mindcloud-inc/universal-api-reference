# Delete Experience Field Value with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId/values/:experienceFieldValueId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Experience Field Value](https://developers.gobridgit.com/reference/experiencefieldvalues_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `experienceFieldId` | path | `string` | yes | The Experience Field UUID |
| `experienceFieldValueId` | path | `string` | yes | The Field Value ID UUID |
