# Alpha TransForm: Change Form Instance Data

Updates data for a form instance in Alpha TransForm.

```
PUT https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/change-form-instance-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/change-form-instance-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formInstanceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/change-form-instance-data', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formInstanceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formInstanceId` | string | yes | formInstanceId of the form instance whose data should be changed |
| `formDataJson` | string | no | Updated form data for the form instance |
| `status` | string | no | updated form status - if blank, then the status is not changed |
| `person` | string | no | person to whom form is assigned - if blank, the person is not changed |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alpha TransForm API returns.

## Native endpoint

Through the native Alpha TransForm API, this operation is `POST /ChangeFormInstanceData/:formInstanceId` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-form-instance-data.md) for the provider-specific parameters and requirements.

