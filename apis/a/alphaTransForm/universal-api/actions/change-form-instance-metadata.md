# Alpha TransForm: Change Form Instance Metadata

Updates form instance metadata in Alpha TransForm.

```
PUT https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/change-form-instance-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/change-form-instance-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formInstanceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/change-form-instance-metadata', {
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
| `formInstanceId` | string | yes | formInstanceId of the form instance whose meta data should be changed |
| `status` | string | no | updated form status - if blank, then the status is not changed |
| `person` | string | no | person to whom form is assigned - if blank, the person is not changed. If ^blank^, person is set to blank |
| `duedate` | string | no | due date for the form. Use yyyy-MM-dd format. If ^blank^, set to blank. |
| `user1` | string | no | User field |
| `user2` | string | no | User field |
| `user3` | string | no | User field |
| `user4` | string | no | User field |
| `user5` | string | no | User field |
| `userlabel1` | string | no | User field |
| `userlabel2` | string | no | User field |
| `userlabel3` | string | no | User field |
| `userlabel4` | string | no | User field |
| `userlabel5` | string | no | User field |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alpha TransForm API returns.

## Native endpoint

Through the native Alpha TransForm API, this operation is `POST /ChangeFormInstanceMetaData/:formInstanceId` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-form-instance-metadata.md) for the provider-specific parameters and requirements.

