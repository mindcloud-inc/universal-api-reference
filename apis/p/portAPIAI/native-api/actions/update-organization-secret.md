# Update Organization Secret with Port API AI

Updates an organization secret in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organization/secrets/:secret_name`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Organization Secret](https://docs.port.io/api-reference/update-an-organization-secret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `secret_name` | path | `string` | yes | The Port organization secret name. |
| `secretValue` | body | `string` | yes | The updated organization secret value. |
