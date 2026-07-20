# Delete Template with Transloadit

Deletes an existing template from Transloadit.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/templates/:templateId`
- **Base URL:** `https://api2.transloadit.com`
- **Official documentation:** [Delete Template](https://transloadit.com/docs/api/templates-template-id-delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | The ID of the template to delete. |
| `params` | body | `string` | yes | JSON string required by Transloadit for template deletion requests. |
