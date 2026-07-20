# LoginRadius: Retrieve User

Retrieves a user profile from LoginRadius.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-user?connectionId=$CONNECTION_ID&accessToken=Access%20token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessToken": "Access token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-user?${params}`, {
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
| `accessToken` | string | yes | Access token for the logged-in user. Example: `Access token`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedDate": "2026-05-07T12:00:00.000Z",
      "Email": [
        {}
      ],
      "EmailVerified": true,
      "ID": "string",
      "IsActive": true,
      "ModifiedDate": "2026-05-07T12:00:00.000Z",
      "ProfileModifiedDate": "2026-05-07T12:00:00.000Z",
      "Provider": "string",
      "Uid": "string",
      "UnverifiedEmail": [
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
| `CreatedDate` | date | When the account was created. |
| `Email` | array<object> | Primary email entries on the profile. |
| `EmailVerified` | boolean | Whether the primary email is verified. |
| `ID` | string | Internal LoginRadius account id. |
| `IsActive` | boolean | Whether the account is active. |
| `ModifiedDate` | date | When the account record was last modified. |
| `ProfileModifiedDate` | date | When the profile was last modified. |
| `Provider` | string | Primary login provider. |
| `Uid` | string | LoginRadius user uid. |
| `UnverifiedEmail` | array<object> | Unverified email entries on the profile. |

## Native endpoint

Through the native LoginRadius API, this operation is `GET /identity/v2/auth/account` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

