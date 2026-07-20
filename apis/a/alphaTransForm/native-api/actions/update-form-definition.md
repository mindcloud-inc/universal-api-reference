# Update Form Definition with Alpha TransForm

Updates an existing form definition in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/UpdateFormDefinitionForFormId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Update Form Definition](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/UpdateFormDefinitionForFormId.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | body | `string` | no | Form definition id. |
| `formDefinition` | body | `object` | no | JSON object with properties to be updated in a TransForm form definition. |
