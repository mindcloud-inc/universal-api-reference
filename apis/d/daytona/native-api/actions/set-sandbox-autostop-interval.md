# Set Sandbox Autostop Interval with Daytona

Updates the sandbox autostop interval in Daytona.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandbox/[:sandboxIdOrName]/autostop/[:interval]`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Set Sandbox Autostop Interval](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxIdOrName` | path | `string` | yes | Sandbox ID or name. |
| `interval` | path | `number` | yes | Auto-stop interval in minutes. |
