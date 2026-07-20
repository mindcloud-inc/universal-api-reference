# Set Sandbox Timeout with E2B

Sets a sandbox timeout in E2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandboxes/{sandboxID}/timeout`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Set Sandbox Timeout](https://e2b.dev/docs/api-reference/sandboxes/set-sandbox-timeout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxID` | path | `string` | yes | Identifier of the sandbox. |
| `timeout` | body | `number` | yes | Timeout in seconds from now after which the sandbox should expire. |
