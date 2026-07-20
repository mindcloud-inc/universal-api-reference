# Monetizze: Generate Access Token

Retrieves an API access token from Monetizze.

```
GET https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/generate-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monetizze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/generate-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/generate-access-token?${params}`, {
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
      "expire": "2026-05-07T12:00:00.000Z",
      "token": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expire` | date | Token expiration timestamp. |
| `token` | string | Temporary Monetizze API token. |
| `user_id` | string | Monetizze user id returned with the generated token. |

## Native endpoint

Through the native Monetizze API, this operation is `GET /token` (base URL `https://api.monetizze.com.br/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-access-token.md) for the provider-specific parameters and requirements.

