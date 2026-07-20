# Create Secret with Infisical

Creates a new secret in a project environment in Infisical.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/secrets/:secretName`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Create Secret](https://infisical.com/docs/api-reference/endpoints/secrets/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `secretName` | path | `string` | yes |
| `projectId` | body | `string` | yes |
| `environment` | body | `string` | yes |
| `secretValue` | body | `string` | yes |
