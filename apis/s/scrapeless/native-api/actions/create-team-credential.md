# Create Team Credential with Scrapeless

Creates a new team credential in Scrapeless.

## Endpoint

- **Method:** `POST`
- **Path:** `/browser/credentials`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Create Team Credential](https://apidocs.scrapeless.com/api-23850715)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-api-token` | query | `string` | no | API key for authentication |
| `origin` | body | `string` | yes | The origin URL (domain) for which these credentials apply |
| `namespace` | body | `string` | no | Optional namespace for credential organization (e.g., 'production', 'staging', 'development') |
| `metadata` | body | `object` | yes | Credential metadata containing authentication data such as username, password, API keys, etc. |
