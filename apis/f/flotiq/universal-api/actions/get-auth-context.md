# Flotiq: Get Auth Context

Retrieves your current Flotiq authentication context.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-auth-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-auth-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-auth-context?${params}`, {
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
      "organization": {},
      "space": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organization` | object | The current Flotiq organization context. |
| `space` | object | The current Flotiq space context. |
| `user` | object | The authenticated user context. |

## Native endpoint

Through the native Flotiq API, this operation is `GET https://api.flotiq.com/api/auth-context` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-context.md) for the provider-specific parameters and requirements.

