# AbcSubmit: Change Password

Updates a user's password in AbcSubmit.

```
PUT https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/change-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/change-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "oldPassword": "string",
  "newPassword": "string",
  "confirmPassword": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/change-password', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "oldPassword": "string",
    "newPassword": "string",
    "confirmPassword": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `oldPassword` | string | yes | The current password for the authenticated AbcSubmit account. |
| `newPassword` | string | yes | The new password to apply to the authenticated account. |
| `confirmPassword` | string | yes | Repeat the new password for confirmation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | boolean |  |

## Native endpoint

Through the native AbcSubmit API, this operation is `POST /api/v1/users/change-password` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-password.md) for the provider-specific parameters and requirements.

