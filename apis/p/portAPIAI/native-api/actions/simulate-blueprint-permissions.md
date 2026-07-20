# Simulate Blueprint Permissions with Port API AI

Retrieves simulated blueprint permissions from Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/blueprints/:blueprint_identifier/permissions/simulate`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Simulate Blueprint Permissions](https://docs.port.io/api-reference/simulate-permissions-for-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The blueprint identifier. |
| `operation` | body | `string` | yes | The operation to simulate. |
| `userIdentifier` | body | `string` | yes | The user identifier to simulate permissions for. |
