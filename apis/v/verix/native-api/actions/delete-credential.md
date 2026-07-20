# Delete Credential with Verix

Deletes an unissued credential from Verix.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/credentials/:credential_id/`
- **Base URL:** `https://api.verix.io`
- **Official documentation:** [Delete Credential](https://docs.verix.io/verifiable_credentials_apis/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credential_id` | path | `string` | yes | Credential ID to delete. |
