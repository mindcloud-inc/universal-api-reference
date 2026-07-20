# Delete Template with Carbone.io

Deletes a template from Carbone.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/template/[:templateId-or-versionId]`
- **Base URL:** `https://api.carbone.io`
- **Official documentation:** [Delete Template](https://carbone.io/documentation/developer/http-api/manage-templates.html#delete-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId-or-versionId` | path | `string` | yes | Template ID (64-bit) or Version ID (SHA-256) to delete. |
