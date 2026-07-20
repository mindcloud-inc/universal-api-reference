# Create, Issue, and Send Credential with Certifier

Creates, issues, and sends a credential in Certifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/credentials/create-issue-send`
- **Base URL:** `https://api.certifier.io/v1`
- **Official documentation:** [Create, Issue, and Send Credential](https://developers.certifier.io/docs/api-reference/credentials/create-issue-and-send-a-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | — |
| `recipient` | body | `object` | yes | — |
| `recipient.name` | body | `string` | yes | — |
| `recipient.email` | body | `string` | no | — |
| `issueDate` | body | `date` | no | Use YYYY-MM-DD. |
| `expiryDate` | body | `date` | no | Use YYYY-MM-DD. |
| `customAttributes` | body | `object` | no | Key-value map of custom attribute tags to values. |
