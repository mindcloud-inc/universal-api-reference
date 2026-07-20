# Change Form Instance Data with Alpha TransForm

Updates data for a form instance in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/ChangeFormInstanceData/:formInstanceId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Change Form Instance Data](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/ChangeFormInstanceData.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formInstanceId` | path | `string` | yes | formInstanceId of the form instance whose data should be changed |
| `formDataJSON` | body | `string` | no | Updated form data for the form instance |
| `status` | body | `string` | no | updated form status - if blank, then the status is not changed |
| `person` | body | `string` | no | person to whom form is assigned - if blank, the person is not changed |
