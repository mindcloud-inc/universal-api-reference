# Buildkite: Get Current Access Token

Retrieves the current access token from Buildkite.

```
GET https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-current-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-current-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-current-access-token?${params}`, {
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
      "createdAt": "string",
      "description": "string",
      "expiresAt": "string",
      "scopes": [
        "string"
      ],
      "user": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `expiresAt` | string |  |
| `scopes` | array<string> |  |
| `user.email` | string |  |
| `user.name` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Buildkite API, this operation is `GET /access-token` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-access-token.md) for the provider-specific parameters and requirements.

