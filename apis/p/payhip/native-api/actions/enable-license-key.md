# Enable License Key with Payhip

Enables an existing license key in Payhip.

## Endpoint

- **Method:** `PUT`
- **Path:** `/license/enable`
- **Base URL:** `https://payhip.com/api/v2`
- **Official documentation:** [Enable License Key](https://payhip.com/api-reference/license-keys/enable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `license_key` | body | `string` | yes | The Payhip license key to enable. |
