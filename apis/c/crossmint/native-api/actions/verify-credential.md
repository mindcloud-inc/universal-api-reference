# Verify Credential with Crossmint

Verifies a credential in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1-alpha1/credentials/verification/verify`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Verify Credential](https://docs.crossmint.com/api-reference/verifiable-credentials/credentials/verify-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credential` | body | `object` | yes | Credential object to verify. |
