# Create Credential Template with Crossmint

Creates a credential template in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1-alpha1/credentials/templates`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Create Credential Template](https://docs.crossmint.com/api-reference/verifiable-credentials/templates/create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | body | `object` | yes | Template metadata object. Provide `name`, `description`, and `imageUrl`. |
| `chain` | body | `string` | yes | Chain for the credential NFT. Crossmint documents values such as `polygon`, `optimism`, and `base`. |
| `credentials` | body | `object` | yes | Credential template configuration object. Include `type`, `storage`, and `encryption`. |
