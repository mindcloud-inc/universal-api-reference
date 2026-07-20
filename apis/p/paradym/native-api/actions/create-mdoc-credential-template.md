# Create Mdoc Credential Template with Paradym

Creates an mdoc credential template in Paradym.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/templates/credentials/mdoc`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Create Mdoc Credential Template](https://paradym.id/reference#tag/mdoc-credential-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Template name. |
| `description` | body | `string` | no | Optional template description. |
| `type` | body | `string` | yes | Credential type identifier for the mdoc template. |
| `validUntil.future.years` | body | `number` | yes | Number of years after issuance that the credential remains valid. |
| `issuer.keyType` | body | `string` | yes | Certificate key type used for issuance. Accepted values: `0`, `1`. |
| `attributes` | body | `object` | yes | Attributes schema object keyed by credential namespace. Example: {"org.mindcloud.test.card":{"properties":{"fullName":{"type":"string","name":"Full Name","required":true}}}} |
