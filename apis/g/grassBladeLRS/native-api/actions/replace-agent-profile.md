# Replace Agent Profile with GrassBlade LRS

Replaces an agent profile in GrassBlade LRS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/agents/profile`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Replace Agent Profile](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentprofres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agent` | query | `string` | yes |
| `profileId` | query | `string` | yes |
| `document` | body | `object` | yes |
