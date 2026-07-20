# Get Encrypted License File with KEYZY

Validates a KEYZY license and retrieves an encrypted license file.

## Endpoint

- **Method:** `POST`
- **Path:** `/licenses/encrypted-file`
- **Base URL:** `https://api.keyzy.io/v2`
- **Official documentation:** [Get Encrypted License File](https://www.keyzy.io/docs/developers/rest-api/licenses-encrypted-file/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | A product code. |
| `device_tag` | body | `string` | no | An operating system and bits information string. |
| `host_id` | body | `string` | no | An id to recognize the device. |
| `serial` | body | `string` | yes | A license serial number to validate. |
