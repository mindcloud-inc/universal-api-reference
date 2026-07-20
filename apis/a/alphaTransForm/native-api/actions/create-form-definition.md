# Create Form Definition with Alpha TransForm

Creates a new form definition in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/CreateNewFormDefinition`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Create Form Definition](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/CreateNewFormDefinition.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | body | `string` | no | formId of the new form definition. Must be unique within the TransForm account |
| `formname` | body | `string` | no | descriptive name of the form |
| `formDefinitionJSON` | body | `string` | no | The JSON definition of the form. You can optionally supply just the form definition commands (i.e. omit meta data). |
