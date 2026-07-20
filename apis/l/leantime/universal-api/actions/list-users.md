# Leantime: List Users



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-users?${params}`, {
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
| `params.activeOnly` | boolean | no | Limit the response to active users only. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1,
      "clientName": {},
      "department": "string",
      "firstname": "Ava",
      "id": 1,
      "jobLevel": "string",
      "jobTitle": "string",
      "lastname": "Chen",
      "modified": "string",
      "profileId": "string",
      "role": "string",
      "status": "string",
      "twoFAEnabled": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number |  |
| `clientName` | object |  |
| `department` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `jobLevel` | string |  |
| `jobTitle` | string |  |
| `lastname` | string |  |
| `modified` | string |  |
| `profileId` | string |  |
| `role` | string |  |
| `status` | string |  |
| `twoFAEnabled` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

