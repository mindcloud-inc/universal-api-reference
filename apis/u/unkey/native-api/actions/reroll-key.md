# Reroll Key with Unkey

Rerolls an existing API key in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/keys.rerollKey`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Reroll Key](https://unkey.com/docs/api-reference/keys/reroll-key)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keyId` | body | `string` | yes |
| `expiration` | body | `number` | yes |
