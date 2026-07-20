# Client Commander: Get Current User

Retrieves the current user from Client Commander.

```
GET https://connect.mindcloud.co/v1/universal/clientCommander/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Client Commander `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientCommander/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clientCommander/latest/actions/get-current-user?${params}`, {
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
      "data": {
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "role": "string",
        "teams": [
          {
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      },
      "meta": {
        "requestId": "string",
        "timestamp": "string",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.avatarUrl` | string |  |
| `data.email` | string |  |
| `data.firstName` | string |  |
| `data.id` | string |  |
| `data.lastName` | string |  |
| `data.role` | string |  |
| `data.teams` | array<object> |  |
| `data.teams[].id` | string |  |
| `data.teams[].name` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |
| `meta.timestamp` | string |  |
| `meta.version` | string |  |

## Native endpoint

Through the native Client Commander API, this operation is `GET /me` (base URL `https://api.clientcommander.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

