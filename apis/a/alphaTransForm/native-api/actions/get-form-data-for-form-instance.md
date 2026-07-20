# Get Form Data For Form Instance with Alpha TransForm

Retrieves form data for a form instance in Alpha TransForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetFormDataForFormInstanceId/:formInstanceId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Get Form Data For Form Instance](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormDataForFormInstanceId.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formInstanceId` | path | `string` | yes | Id of the form instance |
| `mode` | query | `string` | no | "Detailed or "Summary" - determines if form meta data and data or just form meta data are returned.Detailedreturns both meta data and form data |
| `Summary` | query | `string` | no | returns only the form meta data |
