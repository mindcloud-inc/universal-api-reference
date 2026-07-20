# Bytesafe: Get Authenticated User

Retrieves the authenticated user from your Bytesafe workspace.

```
GET https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bytesafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/get-authenticated-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "groups": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "plan": "string",
      "role": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `groups` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `plan` | string |  |
| `role` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Bytesafe API, this operation is `GET /whoami` (base URL `https://mindcloud.bytesafe.dev/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

