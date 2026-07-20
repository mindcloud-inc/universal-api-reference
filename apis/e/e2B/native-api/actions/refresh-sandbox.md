# Refresh Sandbox with E2B

Refreshes a sandbox in E2B, extending its time to live.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandboxes/{sandboxID}/refreshes`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Refresh Sandbox](https://e2b.dev/docs/api-reference/sandboxes/refresh-sandbox)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxID` | path | `string` | yes | Identifier of the sandbox. |
