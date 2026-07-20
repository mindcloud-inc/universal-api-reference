# Configure 1Password Integration with Scrapeless

Updates the 1Password integration in Scrapeless.

## Endpoint

- **Method:** `PUT`
- **Path:** `/browser/one-password/token`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Configure 1Password Integration](https://apidocs.scrapeless.com/api-23850711)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-api-token` | query | `string` | no | API key for authentication |
| `name` | body | `string` | yes | Integration name used to identify this 1Password integration configuration |
| `token` | body | `string` | yes | 1Password API access token for securely accessing your 1Password vault. This should be a service account token starting with 'ops_' |
