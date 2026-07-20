# Update Bitlink with Bitly

Updates an existing bitlink in Bitly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bitlinks/:bitlink`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Update Bitlink](https://dev.bitly.com/api-reference#updateBitlink)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `bitlink` | path | `string` | yes |
| `title` | body | `string` | no |
