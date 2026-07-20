# Alpha TransForm: List Form Instances Across All Forms

Retrieves form instance data across all forms in Alpha TransForm.

```
GET https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/list-form-instances-across-all-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/list-form-instances-across-all-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/list-form-instances-across-all-forms?${params}`, {
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
| `person` | string | no | userId of the TransForm user. If blank form instances for all users are returned |
| `pageSize` | number | no | The number of forms per page. Maximum allowed page size is 200. |
| `pageNumber` | number | no | The page number for which data is returned |
| `mode` | string | no | detailed/summary - determines if meta data and form data or just form instanceId and date created are returned |
| `getRecordCount` | boolean | no | if true, count of number of records is returned |
| `timestamp` | string | no | timestamp when record was last updated. Format is yyyy-mm-dd 0h:0m:0s |
| `fieldlist` | string | no | a list of the top level form fields that you want to return data from. if blank then data for all form fields are returned. |
| `resolveMediaFields` | boolean | no | determine if coded data for media fields is resolved to the actual URL on Amazon S3. |
| `returnMediaFileList` | boolean | no | specify if an array of media files should be returned - only honored if 'resolveMediaFields' is not true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /GetFormInstancesArrayForAllForms` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-instances-across-all-forms.md) for the provider-specific parameters and requirements.

