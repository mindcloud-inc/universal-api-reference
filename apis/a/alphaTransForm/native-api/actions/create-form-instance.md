# Create Form Instance with Alpha TransForm

Creates a new form instance in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/CreateNewFormInstance`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Create Form Instance](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/CreateNewFormInstance.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | body | `string` | no | formId of the form definition for which a new formInstance will be created |
| `formDataJSON` | body | `string` | no | JSON data for the new formInstance |
| `person` | body | `string` | no | the userId for the TransForm user to whom the new formInstnce is assigned. |
