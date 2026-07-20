# Range: Get Auth User

Retrieve the authenticated user and active organization session details.

```
GET https://connect.mindcloud.co/v1/universal/range/latest/actions/get-auth-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/range/latest/actions/get-auth-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/range/latest/actions/get-auth-user?${params}`, {
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
      "accessToken": "string",
      "cues": {},
      "intercomUserHash": "string",
      "loginExpiresAt": "string",
      "org": {},
      "permissions": {},
      "sessionExpiresAt": "string",
      "sessionMaxAge": 1,
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `cues` | object |  |
| `intercomUserHash` | string |  |
| `loginExpiresAt` | string |  |
| `org` | object |  |
| `permissions` | object |  |
| `sessionExpiresAt` | string |  |
| `sessionMaxAge` | number |  |
| `user` | object |  |

## Native endpoint

Through the native Range API, this operation is `GET /v1/users/auth-user` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-user.md) for the provider-specific parameters and requirements.

