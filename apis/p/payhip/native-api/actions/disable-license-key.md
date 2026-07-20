# Disable License Key with Payhip

Disables an existing license key in Payhip.

## Endpoint

- **Method:** `PUT`
- **Path:** `/license/disable`
- **Base URL:** `https://payhip.com/api/v2`
- **Official documentation:** [Disable License Key](https://payhip.com/api-reference/license-keys/disable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `license_key` | body | `string` | yes | The Payhip license key to disable. |
