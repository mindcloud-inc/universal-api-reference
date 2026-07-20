# Create Credential Type with Name with Crossmint

Creates a credential type with a name in Crossmint.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1-alpha1/credentials/types/:typeName`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Create Credential Type with Name](https://docs.crossmint.com/api-reference/verifiable-credentials/types/create-named-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `typeName` | path | `string` | yes | The name of the credential type. |
| `$schema` | body | `string` | yes | JSON Schema draft URL. Crossmint documents `https://json-schema.org/draft/2020-12/schema`. |
| `title` | body | `string` | yes | Credential type title. |
| `description` | body | `string` | no | Credential type description. |
| `type` | body | `string` | yes | Top-level JSON Schema type. The docs example uses `object`. |
| `properties` | body | `object` | yes | Credential schema properties object. Include at least a `credentialSubject` object definition. |
