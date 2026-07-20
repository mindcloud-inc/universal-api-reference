# Alpha TransForm: List Form Instances For Form

Retrieves form instance data for a form in Alpha TransForm.

```
GET https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/list-form-instances-for-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/list-form-instances-for-form?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/list-form-instances-for-form?${params}`, {
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
| `fieldList` | string | no |  |
| `formId` | string | yes | FormId of the form definition |
| `pageSize` | number | no | The number of forms per page. Maximum allowed page size is 200. |
| `pageNumber` | number | no | The page number for which data is returned |
| `mode` | string | no | detailed/summary - determines if form meta data and data or just form instanceId and date created are returned |
| `resolveMediaFields` | boolean | no | determine if coded values for media fields are resolved to the actual URL on Amazon S3. |
| `getRecordCount` | boolean | no | if true, count of number of records is returned |
| `timestamp` | string | no | timestamp (format yyyy-mm-dd 0h:0m:0s). If blank all records are returned. If not blank only records > timestamp are returned. You can prefix with timestamp value with '>=' to return records greater or equal to the timestamp value |
| `fieldlist` | string | no | a list of the top level form fields that you want to return data from. if blank then data for all form fields are returned. |
| `returnMediaFileList` | boolean | no | specify if an array of media files should be returned - only honored if 'resolveMediaFields' is not true. |
| `getFormDefinition` | boolean | no | specify if the form definition should also be returned |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alpha TransForm API returns.

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /GetFormInstancesArrayForFormId/:formId` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-instances-for-form.md) for the provider-specific parameters and requirements.

