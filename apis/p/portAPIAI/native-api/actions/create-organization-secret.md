# Create Organization Secret with Port API AI

Creates an organization secret in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/organization/secrets`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Create Organization Secret](https://docs.port.io/api-reference/create-an-organization-secret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `secretName` | body | `string` | yes | The organization secret name. |
| `secretValue` | body | `string` | yes | The organization secret value. |
