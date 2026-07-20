# Shorten Link with Bitly

Creates a shortened link in Bitly.

## Endpoint

- **Method:** `POST`
- **Path:** `/shorten`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Shorten Link](https://dev.bitly.com/api-reference#createBitlink)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | The Bitly or branded short domain to use. |
| `force_new_link` | body | `boolean` | no | Create a new link even if the long URL was shortened before. |
| `group_guid` | body | `string` | no | The group GUID that should own the new bitlink. |
| `long_url` | body | `string` | yes | The destination URL to shorten. |
