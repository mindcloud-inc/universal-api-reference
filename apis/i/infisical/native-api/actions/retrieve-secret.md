# Retrieve Secret with Infisical

Retrieves a secret from a project environment in Infisical.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v4/secrets/:secretName`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Retrieve Secret](https://infisical.com/docs/api-reference/endpoints/secrets/read)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `secretName` | path | `string` | yes |
| `projectId` | query | `string` | yes |
| `environment` | query | `string` | yes |
