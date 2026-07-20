# Delete State Document with GrassBlade LRS

Deletes a state document from GrassBlade LRS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/activities/state`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Delete State Document](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | query | `string` | yes |
| `agent` | query | `string` | yes |
| `stateId` | query | `string` | yes |
| `registration` | query | `string` | no |
