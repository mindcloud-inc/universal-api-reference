# Microsoft Entra: Create User



```
POST https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Entra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Ava T.",
  "passwordProfile.password": "string",
  "userPrincipalName": "ava@contoso.com",
  "mailNickname": "ava",
  "accountEnabled": "false",
  "passwordProfile": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Ava T.",
    "passwordProfile.password": "string",
    "userPrincipalName": "ava@contoso.com",
    "mailNickname": "ava",
    "accountEnabled": "false",
    "passwordProfile": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayName` | string | yes | Example: `Ava T.`. |
| `passwordProfile.password` | string | yes |  |
| `passwordProfile.forceChangePasswordNextSignIn` | boolean | no | Example: `true`. |
| `userPrincipalName` | string | yes | The domain must be a verified domain in your tenant. Example: `ava@contoso.com`. |
| `mailNickname` | string | yes | Example: `ava`. |
| `accountEnabled` | boolean | yes | Example: `false`. |
| `passwordProfile` | object | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `onPremisesImmutableId` | string | no | Required when the user's sign-in domain is federated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "givenName": "Ava",
      "id": "string",
      "jobTitle": "string",
      "mail": "ava@example.com",
      "mobilePhone": "string",
      "officeLocation": "string",
      "preferredLanguage": "string",
      "surname": "Chen",
      "userPrincipalName": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `jobTitle` | string |  |
| `mail` | string |  |
| `mobilePhone` | string |  |
| `officeLocation` | string |  |
| `preferredLanguage` | string |  |
| `surname` | string |  |
| `userPrincipalName` | string |  |

## Native endpoint

Through the native Microsoft Entra API, this operation is `POST /users` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

