# Validate License with KEYZY

Validates a software license in KEYZY.

## Endpoint

- **Method:** `POST`
- **Path:** `/licenses/valid`
- **Base URL:** `https://api.keyzy.io/v2`
- **Official documentation:** [Validate License](https://www.keyzy.io/docs/developers/rest-api/licenses-validate/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | A product code. |
| `device_tag` | body | `string` | no | An operating system and bits information string. |
| `host_id` | body | `string` | no | An id to recognize the device. |
| `serial` | body | `string` | yes | A license serial number to validate. |
| `version` | body | `string` | yes | Constant value required by KEYZY. Use 2.0. |
