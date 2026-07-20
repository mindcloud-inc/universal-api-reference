# Get Agent Profile with GrassBlade LRS

Retrieves an agent profile from GrassBlade LRS.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/profile`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Get Agent Profile](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentprofres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agent` | query | `string` | yes |
| `profileId` | query | `string` | yes |
