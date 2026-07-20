# Make: Get Current Authorization

Returns current authorization details for the authenticated user, including the token scopes and authentication method used.

```
GET https://connect.mindcloud.co/v1/universal/make/latest/actions/get-current-authorization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Make `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/make/latest/actions/get-current-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/make/latest/actions/get-current-authorization?${params}`, {
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
      "authUsed": "string",
      "scope": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authUsed` | string | Authentication mode used by Make. |
| `scope` | array<string> | Scopes granted to the API token. |

## Native endpoint

Through the native Make API, this operation is `GET /users/me/current-authorization` (base URL `https://us2.make.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-authorization.md) for the provider-specific parameters and requirements.

