# LoginRadius: Create Account

Creates a new account in LoginRadius.

```
POST https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "user@example.com",
  "password": "StrongPassword123!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "user@example.com",
    "password": "StrongPassword123!"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Primary email address for the new account. Example: `user@example.com`. |
| `password` | string | yes | Password for the new account. Example: `StrongPassword123!`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedDate": "2026-05-07T12:00:00.000Z",
      "EmailVerified": true,
      "ID": "string",
      "IsActive": true,
      "ModifiedDate": "2026-05-07T12:00:00.000Z",
      "Provider": "string",
      "RegistrationSource": "string",
      "Uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedDate` | date | When the account was created. |
| `EmailVerified` | boolean | Whether the primary email is verified. |
| `ID` | string | Internal LoginRadius account id. |
| `IsActive` | boolean | Whether the account is active. |
| `ModifiedDate` | date | When the account was last modified. |
| `Provider` | string | Primary account provider. |
| `RegistrationSource` | string | How the account was created. |
| `Uid` | string | Unique LoginRadius user identifier. |

## Native endpoint

Through the native LoginRadius API, this operation is `POST /identity/v2/manage/account` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

