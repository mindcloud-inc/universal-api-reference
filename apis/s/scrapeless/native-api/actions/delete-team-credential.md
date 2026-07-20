# Delete Team Credential with Scrapeless

Deletes a team credential from Scrapeless.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/browser/credentials`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Delete Team Credential](https://apidocs.scrapeless.com/api-23850717)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-api-token` | query | `string` | no | API key for authentication |
| `origin` | body | `string` | yes | The origin URL (domain) for which credentials are stored |
| `namespace` | body | `string` | no | Optional namespace for credential organization (e.g., 'production', 'staging', 'development') |
