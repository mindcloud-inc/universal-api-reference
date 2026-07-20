# Create Sandbox Snapshot with E2B

Creates a snapshot from a sandbox in E2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandboxes/{sandboxID}/snapshots`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Create Sandbox Snapshot](https://e2b.dev/docs/api-reference/sandboxes/post-sandboxes-snapshots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxID` | path | `string` | yes | Identifier of the sandbox. |
