# Replay Assembly with Transloadit

Replays an existing assembly in Transloadit.

## Endpoint

- **Method:** `POST`
- **Path:** `/assemblies/:assemblyId/replay`
- **Base URL:** `https://api2.transloadit.com`
- **Official documentation:** [Replay Assembly](https://transloadit.com/docs/api/assemblies-assembly-id-replay-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assemblyId` | path | `string` | yes | The ID of the assembly to replay. |
| `params` | body | `string` | no | Optional JSON string containing replay parameters supported by Transloadit. |
