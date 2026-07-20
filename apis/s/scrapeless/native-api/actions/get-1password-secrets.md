# Get 1Password Secrets with Scrapeless

Retrieves 1Password secrets from Scrapeless.

## Endpoint

- **Method:** `POST`
- **Path:** `/browser/one-password/secrets`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Get 1Password Secrets](https://apidocs.scrapeless.com/api-23850714)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-api-token` | query | `string` | no | API key for authentication |
| `references[]` | body | `array<string>` | yes | Array of 1Password secret reference paths for batch retrieval of multiple secrets. Each reference format: `op://[vault]/[item]/[field]` |
