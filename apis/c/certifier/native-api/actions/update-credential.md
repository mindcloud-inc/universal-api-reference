# Update Credential with Certifier

Updates an existing credential in Certifier.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/credentials/:id`
- **Base URL:** `https://api.certifier.io/v1`
- **Official documentation:** [Update Credential](https://developers.certifier.io/docs/api-reference/credentials/update-a-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `recipient` | body | `object` | no | — |
| `recipient.id` | body | `string` | no | — |
| `recipient.name` | body | `string` | no | — |
| `recipient.email` | body | `string` | no | — |
| `issueDate` | body | `date` | no | Use YYYY-MM-DD. |
| `expiryDate` | body | `date` | no | Use YYYY-MM-DD. |
| `customAttributes` | body | `object` | no | Key-value map of custom attribute tags to values. |
