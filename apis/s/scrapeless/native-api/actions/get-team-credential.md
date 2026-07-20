# Get Team Credential with Scrapeless

Retrieves a team credential from Scrapeless.

## Endpoint

- **Method:** `GET`
- **Path:** `/browser/credentials`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Get Team Credential](https://apidocs.scrapeless.com/api-23850718)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `origin` | query | `string` | yes | The origin URL (domain) for which credentials are stored |
| `namespace` | query | `string` | no | Optional namespace for credential organization (e.g., 'production', 'staging', 'development') |
| `x-api-token` | query | `string` | no | API key for authentication |
