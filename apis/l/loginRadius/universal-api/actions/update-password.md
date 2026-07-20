# LoginRadius: Update Password

Updates an existing password in LoginRadius.

```
PUT https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/update-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/update-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accessToken": "seeded-access-token",
  "oldPassword": "MindCloud!Stage3#2026",
  "newPassword": "MindCloud!Stage3#2026B"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/update-password', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accessToken": "seeded-access-token",
    "oldPassword": "MindCloud!Stage3#2026",
    "newPassword": "MindCloud!Stage3#2026B"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessToken` | string | yes | Access Token of the user. Example: `seeded-access-token`. |
| `oldPassword` | string | yes | Current password for verification. Example: `MindCloud!Stage3#2026`. |
| `newPassword` | string | yes | New password to set. Example: `MindCloud!Stage3#2026B`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isPosted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isPosted` | boolean | Whether LoginRadius accepted the password update request. |

## Native endpoint

Through the native LoginRadius API, this operation is `PUT /identity/v2/auth/password/change` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-password.md) for the provider-specific parameters and requirements.

