# Update Agent Instructions with echowin

Updates agent instructions in echowin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/agents/:agentId/instructions`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Update Agent Instructions](https://echo.win/api-docs/agents#update-instructions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | path | `string` | yes |
| `instructions` | body | `string` | yes |
