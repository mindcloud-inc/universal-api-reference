# Update Blueprint Permissions with Port API AI

Updates blueprint permissions in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/blueprints/:blueprint_identifier/permissions`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Blueprint Permissions](https://docs.port.io/api-reference/update-a-blueprints-permissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The blueprint identifier. |
| `entities` | body | `object` | yes | Blueprint permissions payload |
