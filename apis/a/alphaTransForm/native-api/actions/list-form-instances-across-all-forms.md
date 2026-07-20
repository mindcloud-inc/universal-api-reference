# List Form Instances Across All Forms with Alpha TransForm

Retrieves form instance data across all forms in Alpha TransForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetFormInstancesArrayForAllForms`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [List Form Instances Across All Forms](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormInstancesArrayForAllForms.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldList` | query | `string` | no | — |
| `person` | query | `string` | no | userId of the TransForm user. If blank form instances for all users are returned |
| `pageSize` | query | `number` | no | The number of forms per page. Maximum allowed page size is 200. |
| `pageNumber` | query | `number` | no | The page number for which data is returned |
| `mode` | query | `string` | no | detailed/summary - determines if meta data and form data or just form instanceId and date created are returned |
| `getRecordCount` | query | `boolean` | no | if true, count of number of records is returned |
| `timestamp` | query | `string` | no | timestamp when record was last updated. Format is yyyy-mm-dd 0h:0m:0s |
| `fieldlist` | query | `string` | no | a list of the top level form fields that you want to return data from. if blank then data for all form fields are returned. |
| `resolveMediaFields` | query | `boolean` | no | determine if coded data for media fields is resolved to the actual URL on Amazon S3. |
| `returnMediaFileList` | query | `boolean` | no | specify if an array of media files should be returned - only honored if 'resolveMediaFields' is not true. |
