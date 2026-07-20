# Create Credential with Certifier

Creates a new credential in Certifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/credentials`
- **Base URL:** `https://api.certifier.io/v1`
- **Official documentation:** [Create Credential](https://developers.certifier.io/docs/api-reference/credentials/create-a-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | — |
| `recipient` | body | `object` | yes | — |
| `recipient.name` | body | `string` | yes | — |
| `recipient.email` | body | `string` | yes | — |
| `issueDate` | body | `date` | no | Use YYYY-MM-DD. |
| `expiryDate` | body | `date` | no | Use YYYY-MM-DD. |
| `customAttributes` | body | `object` | no | Key-value map of custom attribute tags to values. |
