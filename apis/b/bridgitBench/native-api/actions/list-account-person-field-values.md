# List Account Person Field Values with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/Accounts/:id/person-field-values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Account Person Field Values](https://developers.gobridgit.com/reference/accounts_queryprofiles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Account ID |
| `includeEmpty` | query | `boolean` | no | If true, the response will include all person field values, even if no value is set for a given field. If false, field values that are empty are not included in the response. |
| `state` | query | `list<string>` | no | If specified and non-zero, only include field vlaues for people matching the given state. The available values are defined as follows: - active: include only Active people - deactivated: include only Deactivated people - all: include all people, regardless of state Accepted values: `Active`, `All`, `Deactivated`. |
| `personIds` | query | `number` | no | Optional paramater of comma delimited ids for filtering results based on the person IDs provided Send multiple values as a string separated by `,`. |
| `employeeId` | query | `string` | no | Optional - for filtering result by system field "Employee ID" |
