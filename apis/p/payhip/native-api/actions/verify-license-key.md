# Verify License Key with Payhip

Verifies a Payhip license key and returns its details.

## Endpoint

- **Method:** `GET`
- **Path:** `/license/verify`
- **Base URL:** `https://payhip.com/api/v2`
- **Official documentation:** [Verify License Key](https://payhip.com/api-reference/license-keys/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `license_key` | query | `string` | yes | The Payhip license key to verify. |
