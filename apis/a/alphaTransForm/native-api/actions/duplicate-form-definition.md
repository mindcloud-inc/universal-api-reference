# Duplicate Form Definition with Alpha TransForm

Creates a duplicate form definition in Alpha TransForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/DuplicateFormDefinition`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Duplicate Form Definition](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/DuplicateFormDefinition.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | query | `string` | yes | FormId of the form definition to be duplicated |
| `newformId` | query | `string` | yes | FormId for the duplicated form definition |
| `newFormName` | query | `string` | yes | Friendly name for the duplicate form definition |
| `newAccountId` | query | `string` | no | Optional target account for the duplicated form definition |
