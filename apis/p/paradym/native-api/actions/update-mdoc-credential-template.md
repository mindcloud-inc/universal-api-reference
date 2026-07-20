# Update Mdoc Credential Template with Paradym

Updates an mdoc credential template in Paradym.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/templates/credentials/mdoc/:credentialTemplateId`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Update Mdoc Credential Template](https://paradym.id/reference#tag/mdoc-credential-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentialTemplateId` | path | `string` | yes | Template to update. |
| `name` | body | `string` | yes | Template name. |
| `description` | body | `string` | no | Optional template description. |
| `validUntil.future.years` | body | `number` | yes | Number of years after issuance that the credential remains valid. |
| `attributes` | body | `object` | yes | Attributes schema object keyed by credential namespace. Example: {"org.mindcloud.test.card":{"properties":{"fullName":{"type":"string","name":"Full Name","required":true}}}} |
