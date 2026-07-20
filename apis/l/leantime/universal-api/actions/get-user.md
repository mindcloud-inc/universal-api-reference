# Leantime: Get User



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-user?${params}`, {
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
| `userId` | number | yes | The Leantime user id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1,
      "createdOn": "string",
      "department": "string",
      "description": {},
      "expires": {},
      "firstname": "Ava",
      "forcePwReset": {},
      "hours": {},
      "id": 1,
      "jobLevel": "string",
      "jobTitle": "string",
      "lastlogin": {},
      "lastname": "Chen",
      "lastpwdChange": {},
      "modified": "string",
      "notifications": 1,
      "password": "string",
      "phone": "string",
      "profileId": "string",
      "pwReset": "string",
      "pwResetCount": {},
      "pwResetExpiration": {},
      "role": "string",
      "session": {},
      "sessiontime": {},
      "settings": {},
      "source": "string",
      "status": "string",
      "twoFAEnabled": 1,
      "twoFASecret": {},
      "username": "Ava Chen",
      "wage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number |  |
| `createdOn` | string |  |
| `department` | string |  |
| `description` | object |  |
| `expires` | object |  |
| `firstname` | string |  |
| `forcePwReset` | object |  |
| `hours` | object |  |
| `id` | number |  |
| `jobLevel` | string |  |
| `jobTitle` | string |  |
| `lastlogin` | object |  |
| `lastname` | string |  |
| `lastpwdChange` | object |  |
| `modified` | string |  |
| `notifications` | number |  |
| `password` | string |  |
| `phone` | string |  |
| `profileId` | string |  |
| `pwReset` | string |  |
| `pwResetCount` | object |  |
| `pwResetExpiration` | object |  |
| `role` | string |  |
| `session` | object |  |
| `sessiontime` | object |  |
| `settings` | object |  |
| `source` | string |  |
| `status` | string |  |
| `twoFAEnabled` | number |  |
| `twoFASecret` | object |  |
| `username` | string |  |
| `wage` | object |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

