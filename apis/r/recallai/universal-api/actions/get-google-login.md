# Recallai: Get Google Login

Retrieves a Google login from Recallai.

```
GET https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-google-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-google-login?connectionId=$CONNECTION_ID&loginId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "loginId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-google-login?${params}`, {
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
| `loginId` | string | yes | A UUID string identifying this google login. |

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

Through the native Recallai API, this operation is `GET /api/v2/google-logins/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-login.md) for the provider-specific parameters and requirements.

