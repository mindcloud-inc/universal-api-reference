# Edit Template Credential with Transloadit

Updates an existing template credential in Transloadit.

## Endpoint

- **Method:** `PUT`
- **Path:** `/template_credentials/:credentialsId`
- **Base URL:** `https://api2.transloadit.com`
- **Official documentation:** [Edit Template Credential](https://transloadit.com/docs/api/template-credentials-credentials-id-or-name-put/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentialsId` | path | `string` | yes | The ID or name of the template credential to edit. |
| `params` | body | `string` | yes | JSON string containing the updated Transloadit template credential definition. |
