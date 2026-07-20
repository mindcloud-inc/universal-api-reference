# Connect To Sandbox with E2B

Retrieves sandbox details from E2B and resumes it if paused.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandboxes/{sandboxID}/connect`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Connect To Sandbox](https://e2b.dev/docs/api-reference/sandboxes/connect-to-sandbox)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxID` | path | `string` | yes | Identifier of the sandbox. |
