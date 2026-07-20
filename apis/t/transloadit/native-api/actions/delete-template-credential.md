# Delete Template Credential with Transloadit

Deletes an existing template credential from Transloadit.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/template_credentials/:credentialsId`
- **Base URL:** `https://api2.transloadit.com`
- **Official documentation:** [Delete Template Credential](https://transloadit.com/docs/api/template-credentials-credentials-id-or-name-delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentialsId` | path | `string` | yes | The ID or name of the template credential to delete. |
| `params` | body | `string` | yes | JSON string required by Transloadit for template credential deletion requests. |
