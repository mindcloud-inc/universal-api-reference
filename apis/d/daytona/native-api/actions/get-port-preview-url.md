# Get Port Preview URL with Daytona

Retrieves a sandbox port preview URL from Daytona.

## Endpoint

- **Method:** `GET`
- **Path:** `/sandbox/[:sandboxIdOrName]/ports/[:port]/preview-url`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Get Port Preview URL](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxIdOrName` | path | `string` | yes | Sandbox ID or name. |
| `port` | path | `number` | yes | Sandbox port number. |
