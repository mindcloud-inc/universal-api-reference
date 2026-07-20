# Delete Secret with Infisical

Deletes an existing secret from a project environment in Infisical.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v4/secrets/:secretName`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Delete Secret](https://infisical.com/docs/api-reference/endpoints/secrets/delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `secretName` | path | `string` | yes |
| `projectId` | body | `string` | yes |
| `environment` | body | `string` | yes |
