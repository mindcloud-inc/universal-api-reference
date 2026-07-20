# Create Full Bitlink with Bitly

Creates a bitlink in Bitly with additional parameters.

## Endpoint

- **Method:** `POST`
- **Path:** `/bitlinks`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Create Full Bitlink](https://dev.bitly.com/api-reference#createFullBitlink)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_guid` | body | `string` | no |
| `long_url` | body | `string` | yes |
| `title` | body | `string` | no |
