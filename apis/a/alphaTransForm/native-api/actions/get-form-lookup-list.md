# Get Form Lookup List with Alpha TransForm

Retrieves list field choices from Alpha TransForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetFormLookupList`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Get Form Lookup List](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormLookupList.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | query | `string` | no | Form definition id. |
| `fieldName` | query | `string` | no | Field name of the List field. |
