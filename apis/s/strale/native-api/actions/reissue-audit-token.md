# Reissue Audit Token with Strale

Reissues an audit token for a transaction in Strale.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/transactions/:id/audit-token`
- **Base URL:** `https://api.strale.io`
- **Official documentation:** [Reissue Audit Token](https://api.strale.io/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expires_in_days` | body | `number` | no | Number of days before the new audit token expires. |
| `id` | path | `string` | yes | Transaction ID. |
