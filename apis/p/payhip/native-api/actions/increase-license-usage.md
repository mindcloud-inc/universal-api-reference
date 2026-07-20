# Increase License Usage with Payhip

Increases a Payhip license key usage count.

## Endpoint

- **Method:** `PUT`
- **Path:** `/license/usage`
- **Base URL:** `https://payhip.com/api/v2`
- **Official documentation:** [Increase License Usage](https://payhip.com/api-reference/license-keys/usage-increase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `license_key` | body | `string` | yes | The Payhip license key whose usage count should be increased. |
