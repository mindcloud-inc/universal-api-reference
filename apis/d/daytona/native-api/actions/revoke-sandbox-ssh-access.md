# Revoke Sandbox SSH Access with Daytona

Revokes sandbox SSH access in Daytona.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sandbox/[:sandboxIdOrName]/ssh-access`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Revoke Sandbox SSH Access](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxIdOrName` | path | `string` | yes | ID or name of the sandbox. |
