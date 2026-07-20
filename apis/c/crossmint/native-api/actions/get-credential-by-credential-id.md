# Get Credential by Credential ID with Crossmint

Retrieves a credential from Crossmint by credential ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1-alpha1/credentials/:id`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Get Credential by Credential ID](https://docs.crossmint.com/api-reference/verifiable-credentials/credentials/retrieve-credential-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Credential identifier in `urn:uuid:<UUID>` format. |
