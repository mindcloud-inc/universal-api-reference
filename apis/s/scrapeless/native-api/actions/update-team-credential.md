# Update Team Credential with Scrapeless

Updates an existing team credential in Scrapeless.

## Endpoint

- **Method:** `PUT`
- **Path:** `/browser/credentials`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Update Team Credential](https://apidocs.scrapeless.com/api-23850716)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-api-token` | query | `string` | no | API key for authentication |
| `origin` | body | `string` | yes | The origin URL (domain) for which these credentials apply |
| `namespace` | body | `string` | no | Optional namespace for credential organization (e.g., 'production', 'staging', 'development') |
| `metadata` | body | `object` | yes | Updated credential metadata containing authentication data |
