# Authenticate with Infisical

Authenticates with Infisical using Universal Auth.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/auth/universal-auth/login`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Authenticate](https://infisical.com/docs/api-reference/endpoints/universal-auth/login)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | body | `string` | yes | The Infisical machine identity Client ID. |
| `clientSecret` | body | `string` | yes | The Infisical machine identity Client Secret. |
