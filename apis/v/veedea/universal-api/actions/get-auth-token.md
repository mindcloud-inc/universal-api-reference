# Veedea: Get Auth Token

Retrieves an auth token from Veedea.

```
GET https://connect.mindcloud.co/v1/universal/veedea/latest/actions/get-auth-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veedea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veedea/latest/actions/get-auth-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veedea/latest/actions/get-auth-token?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "status": 1,
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Account email returned by the authentication endpoint. |
| `id` | string | Veedea account ID returned by the authentication endpoint. |
| `name` | string | Account name returned by the authentication endpoint. |
| `status` | number | HTTP-style status code returned in the Veedea auth payload. |
| `token` | string | Auth token used by subsequent Veedea API requests. |

## Native endpoint

Through the native Veedea API, this operation is `GET /auth` (base URL `https://veedea.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-token.md) for the provider-specific parameters and requirements.

