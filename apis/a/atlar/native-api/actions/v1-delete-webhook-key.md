# V1 Delete webhook key with Atlar

Deletes an existing webhook key from Atlar v1.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/webhooks/{id}/keys/{keyId}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [V1 Delete webhook key](https://docs.atlar.com/v1/reference/delete_v1-webhooks-id-keys-keyid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `keyId` | path | `string` | yes |
