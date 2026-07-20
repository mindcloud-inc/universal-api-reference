# Replace State Document with GrassBlade LRS

Replaces a state document in GrassBlade LRS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/activities/state`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Replace State Document](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | query | `string` | yes |
| `agent` | query | `string` | yes |
| `stateId` | query | `string` | yes |
| `registration` | query | `string` | no |
| `document` | body | `object` | yes |
