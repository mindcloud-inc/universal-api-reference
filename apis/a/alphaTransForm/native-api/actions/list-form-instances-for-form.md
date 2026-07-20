# List Form Instances For Form with Alpha TransForm

Retrieves form instance data for a form in Alpha TransForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetFormInstancesArrayForFormId/:formId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [List Form Instances For Form](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormInstancesArrayForFormId.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldList` | query | `string` | no | — |
| `formId` | path | `string` | yes | FormId of the form definition |
| `pageSize` | query | `number` | no | The number of forms per page. Maximum allowed page size is 200. |
| `pageNumber` | query | `number` | no | The page number for which data is returned |
| `mode` | query | `string` | no | detailed/summary - determines if form meta data and data or just form instanceId and date created are returned |
| `resolveMediaFields` | query | `boolean` | no | determine if coded values for media fields are resolved to the actual URL on Amazon S3. |
| `getRecordCount` | query | `boolean` | no | if true, count of number of records is returned |
| `timestamp` | query | `string` | no | timestamp (format yyyy-mm-dd 0h:0m:0s). If blank all records are returned. If not blank only records > timestamp are returned. You can prefix with timestamp value with '>=' to return records greater or equal to the timestamp value |
| `fieldlist` | query | `string` | no | a list of the top level form fields that you want to return data from. if blank then data for all form fields are returned. |
| `returnMediaFileList` | query | `boolean` | no | specify if an array of media files should be returned - only honored if 'resolveMediaFields' is not true. |
| `getFormDefinition` | query | `boolean` | no | specify if the form definition should also be returned |
