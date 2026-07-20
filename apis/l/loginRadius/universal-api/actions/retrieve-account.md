# LoginRadius: Retrieve Account

Retrieves an account from LoginRadius by email, username, or phone.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/retrieve-account?${params}`, {
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
| `email` | string | no | Email address to verify availability or retrieve associated Account. Example: `user@example.com`. |
| `username` | string | no | Username to verify availability or retrieve associated Account. Example: `stage3-user`. |
| `phone` | string | no | Phone number to verify availability or retrieve associated Account. Example: `+15551234567`. |
| `q` | string | no | Query filter in key:value format. The key must be an indexed profile field. Example: `Uid:743a88db13d1411b9a0c68d7218f1703`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preventWebhook` | boolean | no | When true, suppresses webhook events for this operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "2026-05-07T12:00:00.000Z",
      "email": [
        {
          "type": "ava@example.com",
          "value": "ava@example.com"
        }
      ],
      "emailVerified": true,
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "isActive": true,
      "isDeleted": true,
      "isLoginLocked": true,
      "lastLoginDate": "2026-05-07T12:00:00.000Z",
      "lastLoginLocation": "string",
      "lastName": "Chen",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "passkeyLogin": {
        "localEnrollmentFlag": true,
        "progressiveFlag": true
      },
      "phoneIdVerified": true,
      "profileModifiedDate": "2026-05-07T12:00:00.000Z",
      "provider": "string",
      "registrationProvider": "string",
      "registrationSource": "string",
      "signupDate": "2026-05-07T12:00:00.000Z",
      "uid": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `email[].type` | string |  |
| `email[].value` | string |  |
| `emailVerified` | boolean |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `isDeleted` | boolean |  |
| `isLoginLocked` | boolean |  |
| `lastLoginDate` | date |  |
| `lastLoginLocation` | string |  |
| `lastName` | string |  |
| `modifiedDate` | date |  |
| `passkeyLogin.localEnrollmentFlag` | boolean |  |
| `passkeyLogin.progressiveFlag` | boolean |  |
| `phoneIdVerified` | boolean |  |
| `profileModifiedDate` | date |  |
| `provider` | string |  |
| `registrationProvider` | string |  |
| `registrationSource` | string |  |
| `signupDate` | date |  |
| `uid` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native LoginRadius API, this operation is `GET /identity/v2/manage/account` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-account.md) for the provider-specific parameters and requirements.

