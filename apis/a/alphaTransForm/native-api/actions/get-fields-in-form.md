# Get Fields In Form with Alpha TransForm

Retrieves form fields from Alpha TransForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetFieldsInForm/:formId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Get Fields In Form](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFieldsInForm.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | FormId of the form definition |
| `includeFieldType` | query | `boolean` | no | true/false - if true the extended field type for each field is shown |
