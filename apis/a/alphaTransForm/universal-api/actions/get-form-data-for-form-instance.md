# Alpha TransForm: Get Form Data For Form Instance

Retrieves form data for a form instance in Alpha TransForm.

```
GET https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-form-data-for-form-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-form-data-for-form-instance?connectionId=$CONNECTION_ID&formInstanceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formInstanceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-form-data-for-form-instance?${params}`, {
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
| `formInstanceId` | string | yes | Id of the form instance |
| `mode` | string | no | "Detailed or "Summary" - determines if form meta data and data or just form meta data are returned.Detailedreturns both meta data and form data |
| `summary` | string | no | returns only the form meta data |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
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
| `result` | array<object> | Contains the information for the form instance. |

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /GetFormDataForFormInstanceId/:formInstanceId` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-data-for-form-instance.md) for the provider-specific parameters and requirements.

