# Expand Bitlink with Bitly

Retrieves the long URL for a Bitly bitlink.

## Endpoint

- **Method:** `POST`
- **Path:** `/expand`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Expand Bitlink](https://dev.bitly.com/api-reference#expandBitlink)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bitlink_id` | body | `string` | no | The Bitly bitlink ID to expand. |
