# Revoke Credential with Crossmint

Revokes a credential in Crossmint.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1-alpha1/credentials/:id`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Revoke Credential](https://docs.crossmint.com/api-reference/verifiable-credentials/credentials/revoke-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Credential identifier in `urn:uuid:<UUID>` format. |
