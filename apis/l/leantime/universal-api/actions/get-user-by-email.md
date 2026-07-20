# Leantime: Get User by Email



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-user-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-user-by-email?connectionId=$CONNECTION_ID&params.email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-user-by-email?${params}`, {
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
| `params.email` | string | yes | The email address to look up. |
| `params.status` | string | no | User status code filter. Default: `a`. |

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

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-by-email.md) for the provider-specific parameters and requirements.

