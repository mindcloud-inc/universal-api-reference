# Set Form Lookup List with Alpha TransForm

Updates list field choices in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/SetFormLookupList/:formId/:fieldName`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Set Form Lookup List](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/SetFormLookupList.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Form definition id. |
| `fieldName` | path | `string` | yes | Field name of the List field. |
| `listdata[]` | body | `array<string>` | no | Choices for the list. Can either be JSON array with 'value' and optional 'text' property, or CRLF list with data in the form displayValue\|storedValue Send multiple values as a array. |
