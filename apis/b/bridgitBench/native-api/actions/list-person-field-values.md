# List Person Field Values with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/person-field-values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Person Field Values](https://developers.gobridgit.com/reference/personfieldvalue_queryfieldvalues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | The Person ID |
| `includeEmpty` | query | `boolean` | no | If true, the response will include all person field values, even if no value is set for a given field. If false, field values that are empty are not included in the response. |
