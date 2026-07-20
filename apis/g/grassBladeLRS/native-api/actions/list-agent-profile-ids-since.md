# List Agent Profile IDs Since with GrassBlade LRS

Retrieves agent profile IDs from GrassBlade LRS since a timestamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/profile`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [List Agent Profile IDs Since](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentprofres)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agent` | query | `string` | yes |
| `since` | query | `string` | yes |
