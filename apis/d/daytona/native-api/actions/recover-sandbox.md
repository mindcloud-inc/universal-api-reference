# Recover Sandbox with Daytona

Recovers a sandbox from an error state in Daytona.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandbox/[:sandboxIdOrName]/recover`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Recover Sandbox](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxIdOrName` | path | `string` | yes | ID or name of the sandbox. |
