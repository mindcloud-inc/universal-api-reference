# Recallai: Update Google Login

Updates an existing Google login in Recallai.

```
PUT https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-google-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-google-login" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "loginId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-google-login', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "loginId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | The email address of the google account to use for login. |
| `groupId` | string | no | The id of the login group this login belongs to. |
| `isActive` | boolean | no | If the login should be used for round robin. (default: true) |
| `loginId` | string | yes | A UUID string identifying this google login. |
| `ssoV2Cert` | string | no | PEM-formatted x509 certificate which is registered in your Google Workspace SSO Profile. |
| `ssoV2PrivateKey` | string | no | PEM-formatted private key used for signing SSO requests. |
| `ssoV2WorkspaceDomain` | string | no | The primary domain name of your Google Workspace Account used for SSO. |

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

Through the native Recallai API, this operation is `PATCH /api/v2/google-logins/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-google-login.md) for the provider-specific parameters and requirements.

