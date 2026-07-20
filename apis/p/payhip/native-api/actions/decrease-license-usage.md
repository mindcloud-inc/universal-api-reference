# Decrease License Usage with Payhip

Decreases a Payhip license key usage count.

## Endpoint

- **Method:** `PUT`
- **Path:** `/license/decrease`
- **Base URL:** `https://payhip.com/api/v2`
- **Official documentation:** [Decrease License Usage](https://payhip.com/api-reference/license-keys/usage-decrease)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `license_key` | body | `string` | yes | The Payhip license key whose usage count should be decreased. |
