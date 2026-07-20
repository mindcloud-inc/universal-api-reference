# ironSource: Get Bearer Token

Retrieves a bearer token from ironSource.

```
GET https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-bearer-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-bearer-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-bearer-token?${params}`, {
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
      "accessToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Bearer token returned by the ironSource authentication endpoint. |

## Native endpoint

Through the native ironSource API, this operation is `GET partners/publisher/auth` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bearer-token.md) for the provider-specific parameters and requirements.

