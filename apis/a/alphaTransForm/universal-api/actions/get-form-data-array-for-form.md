# Alpha TransForm: Get Form Data Array For Form

Retrieves form data for all instances of a form in Alpha TransForm.

```
GET https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-form-data-array-for-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-form-data-array-for-form?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-form-data-array-for-form?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | FormId of the form definition |
| `pageSize` | number | no | The number of forms per page. Maximum allowed page size is 200. |
| `pageNumber` | number | no | The page number for which data is returned |
| `resolveMediaFields` | boolean | no | determine if coded data for media fields is resolved to the actual URL on Amazon S3. |
| `getRecordCount` | boolean | no | if true, count of number of records is returned |
| `timestamp` | string | no | timestamp when record was last updated. Format is yyyy-mm-dd 0h:0m:0s |
| `fieldList` | string | no | a list of the top level form fields that you want to return data from. if blank then data for all form fields are returned. |
| `injectFormMetaDataIntoData` | boolean | no | specifies if form meta data (i.e. name of user filling in form, form status, etc.) should be injected into the formdata return by the method. |
| `otheroptions` | string | no | other options (in a JSON format) |
| `returnMediaFileList` | boolean | no | specify if an array of media files should be returned - only honored if 'resolveMediaFields' is not true. |
| `getFormDefinition` | boolean | no | specify if the form definition should also be returned |
| `formDataFilterJavascript` | number | no | Javascript code to filter the form data. Your Javascript code must return true or false. If true the formdata is included in the return result. Your Javascript code can reference form fields using this syntax: data.formdata.name_of_field (e.g. if(data.formdata.color == 'red') return true; ). If you specify a formdata filter you should also specify a metadata filter to limit that number of rows that need to be searched. |
| `metadatafilter` | string | no | Filter based on meta data fields. Syntax is SQL. E.g.: person = '[email&#160;protected]' and status = 'open' |
| `metadatafilterparameters` | string | no | If the metadata filter uses arguments, supplies the argument values. Format is a crlf delimited string of format value\|\|\|type\|parametername |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alpha TransForm API returns.

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /GetFormDataArrayForFormId/:formId` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-data-array-for-form.md) for the provider-specific parameters and requirements.

