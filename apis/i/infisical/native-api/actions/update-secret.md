# Update Secret with Infisical

Updates an existing secret in a project environment in Infisical.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/secrets/:secretName`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Update Secret](https://infisical.com/docs/api-reference/endpoints/secrets/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `secretName` | path | `string` | yes |
| `projectId` | body | `string` | yes |
| `environment` | body | `string` | yes |
| `secretValue` | body | `string` | yes |
