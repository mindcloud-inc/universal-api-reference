# LoginRadius: Add Email

Adds an email address to a LoginRadius account.

```
POST https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/add-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/add-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accessToken": "Access token",
  "email": "alias@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/add-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accessToken": "Access token",
    "email": "alias@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessToken` | string | yes | Access token for the logged-in user. Example: `Access token`. |
| `email` | string | yes | Additional email address to add to the account. Example: `alias@example.com`. |
| `type` | string | no | Email type label for the new address. Example: `Secondary`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "IsPosted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IsPosted` | boolean | Whether LoginRadius accepted the add-email request. |

## Native endpoint

Through the native LoginRadius API, this operation is `POST /identity/v2/auth/email` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-email.md) for the provider-specific parameters and requirements.

