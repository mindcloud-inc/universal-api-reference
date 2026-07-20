# Create Sandbox SSH Access with Daytona

Creates sandbox SSH access in Daytona.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandbox/[:sandboxIdOrName]/ssh-access`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Create Sandbox SSH Access](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxIdOrName` | path | `string` | yes | ID or name of the sandbox. |
