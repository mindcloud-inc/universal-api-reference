# Delete All State For Context with GrassBlade LRS

Deletes all state documents for a context in GrassBlade LRS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/activities/state`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Delete All State For Context](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | query | `string` | yes |
| `agent` | query | `string` | yes |
| `registration` | query | `string` | yes |
