# Recallai: Create Google Login

Creates a new Google login in Recallai.

```
POST https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-google-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-google-login" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "groupId": "string",
  "ssoV2Cert": "string",
  "ssoV2PrivateKey": "string",
  "ssoV2WorkspaceDomain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-google-login', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "groupId": "string",
    "ssoV2Cert": "string",
    "ssoV2PrivateKey": "string",
    "ssoV2WorkspaceDomain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The email address of the google account to use for login. |
| `groupId` | string | yes | The id of the login group this login belongs to. |
| `isActive` | boolean | no | If the login should be used for round robin. (default: true) |
| `ssoV2Cert` | string | yes | PEM-formatted x509 certificate which is registered in your Google Workspace SSO Profile. |
| `ssoV2PrivateKey` | string | yes | PEM-formatted private key used for signing SSO requests. |
| `ssoV2WorkspaceDomain` | string | yes | The primary domain name of your Google Workspace Account used for SSO. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "email": "ava@example.com",
      "groupId": "string",
      "id": "string",
      "isActive": true,
      "ssoV2Cert": "string",
      "ssoV2PrivateKey": "string",
      "ssoV2WorkspaceDomain": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `email` | string |  |
| `groupId` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `ssoV2Cert` | string |  |
| `ssoV2PrivateKey` | string |  |
| `ssoV2WorkspaceDomain` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `POST /api/v2/google-logins/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-google-login.md) for the provider-specific parameters and requirements.

