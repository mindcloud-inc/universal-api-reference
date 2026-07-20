# Get 1Password Secret with Scrapeless

Retrieves a 1Password secret from Scrapeless.

## Endpoint

- **Method:** `POST`
- **Path:** `/browser/one-password/secret`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Get 1Password Secret](https://apidocs.scrapeless.com/api-23850713)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-api-token` | query | `string` | no | API key for authentication |
| `reference` | body | `string` | yes | 1Password secret reference path in format: `op://[vault]/[item]/[field]`. You can obtain vault ID and item ID from the 1Password admin interface |
