# Appwrite: Create anonymous session

Creates a new anonymous session in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-anonymous-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-anonymous-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-anonymous-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "clientCode": "string",
      "clientEngine": "string",
      "clientEngineVersion": "string",
      "clientName": "Ava Chen",
      "clientType": "string",
      "clientVersion": "string",
      "countryCode": "string",
      "countryName": "Ava Chen",
      "current": true,
      "deviceBrand": "string",
      "deviceModel": "string",
      "deviceName": "Ava Chen",
      "expire": "string",
      "factors": [
        "string"
      ],
      "ip": "string",
      "mfaUpdatedAt": "string",
      "osCode": "string",
      "osName": "Ava Chen",
      "osVersion": "string",
      "provider": "string",
      "providerAccessToken": "string",
      "providerAccessTokenExpiry": "string",
      "providerRefreshToken": "string",
      "providerUid": "string",
      "secret": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Session creation date in ISO 8601 format. |
| `$id` | string | Session ID. |
| `$updatedAt` | string | Session update date in ISO 8601 format. |
| `clientCode` | string | Client code name. View list of [available options](https://github.com/appwrite/appwrite/blob/master/docs/lists/clients.json). |
| `clientEngine` | string | Client engine name. |
| `clientEngineVersion` | string | Client engine name. |
| `clientName` | string | Client name. |
| `clientType` | string | Client type. |
| `clientVersion` | string | Client version. |
| `countryCode` | string | Country two-character ISO 3166-1 alpha code. |
| `countryName` | string | Country name. |
| `current` | boolean | Returns true if this the current user session. |
| `deviceBrand` | string | Device brand name. |
| `deviceModel` | string | Device model name. |
| `deviceName` | string | Device name. |
| `expire` | string | Session expiration date in ISO 8601 format. |
| `factors` | array<string> | Returns a list of active session factors. |
| `ip` | string | IP in use when the session was created. |
| `mfaUpdatedAt` | string | Most recent date in ISO 8601 format when the session successfully passed MFA challenge. |
| `osCode` | string | Operating system code name. View list of [available options](https://github.com/appwrite/appwrite/blob/master/docs/lists/os.json). |
| `osName` | string | Operating system name. |
| `osVersion` | string | Operating system version. |
| `provider` | string | Session Provider. |
| `providerAccessToken` | string | Session Provider Access Token. |
| `providerAccessTokenExpiry` | string | The date of when the access token expires in ISO 8601 format. |
| `providerRefreshToken` | string | Session Provider Refresh Token. |
| `providerUid` | string | Session Provider User ID. |
| `secret` | string | Secret used to authenticate the user. Only included if the request was made with an API key |
| `userId` | string | User ID. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /account/sessions/anonymous` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-create-anonymous-session.md) for the provider-specific parameters and requirements.

