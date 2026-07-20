# List Secrets with Infisical

Retrieves secrets from a project environment in Infisical.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v4/secrets`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [List Secrets](https://infisical.com/docs/api-reference/endpoints/secrets/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `string` | yes | The Infisical project ID to list secrets from. |
| `environment` | query | `string` | yes | The environment slug to list secrets from. |
| `secretPath` | query | `string` | no | The secret path to list secrets from. Defaults to /. |
