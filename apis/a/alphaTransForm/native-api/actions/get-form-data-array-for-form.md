# Get Form Data Array For Form with Alpha TransForm

Retrieves form data for all instances of a form in Alpha TransForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetFormDataArrayForFormId/:formId`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Get Form Data Array For Form](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/GetFormDataArrayForFormId.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | FormId of the form definition |
| `pageSize` | query | `number` | no | The number of forms per page. Maximum allowed page size is 200. |
| `pageNumber` | query | `number` | no | The page number for which data is returned |
| `resolveMediaFields` | query | `boolean` | no | determine if coded data for media fields is resolved to the actual URL on Amazon S3. |
| `getRecordCount` | query | `boolean` | no | if true, count of number of records is returned |
| `timestamp` | query | `string` | no | timestamp when record was last updated. Format is yyyy-mm-dd 0h:0m:0s |
| `fieldList` | query | `string` | no | a list of the top level form fields that you want to return data from. if blank then data for all form fields are returned. |
| `injectFormMetaDataIntoData` | query | `boolean` | no | specifies if form meta data (i.e. name of user filling in form, form status, etc.) should be injected into the formdata return by the method. |
| `otheroptions` | query | `string` | no | other options (in a JSON format) |
| `returnMediaFileList` | query | `boolean` | no | specify if an array of media files should be returned - only honored if 'resolveMediaFields' is not true. |
| `getFormDefinition` | query | `boolean` | no | specify if the form definition should also be returned |
| `formDataFilterJavascript` | query | `number` | no | Javascript code to filter the form data. Your Javascript code must return true or false. If true the formdata is included in the return result. Your Javascript code can reference form fields using this syntax: data.formdata.name_of_field (e.g. if(data.formdata.color == 'red') return true; ). If you specify a formdata filter you should also specify a metadata filter to limit that number of rows that need to be searched. |
| `metadatafilter` | query | `string` | no | Filter based on meta data fields. Syntax is SQL. E.g.: person = '[email&#160;protected]' and status = 'open' |
| `metadatafilterparameters` | query | `string` | no | If the metadata filter uses arguments, supplies the argument values. Format is a crlf delimited string of format value\|\|\|type\|parametername |
