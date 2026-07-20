# Create API Key with Documo

Creates a new API key in Documo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-keys`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Create API Key](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access` | body | `string` | yes | String \| Required \| Possible values: admin, base, print_driver |
| `name` | body | `string` | no | String \| 128 characters limit \| Key name \| Default: null |
| `userId` | body | `string` | no | Uuid \| User id that will be assigned to key \| Default: current user |
| `expiresAt` | body | `string` | no | String \| Expire date |
