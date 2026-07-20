# Timewax: Get Authentication Token

Retrieves an authentication token from Timewax.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-authentication-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-authentication-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/get-authentication-token?${params}`, {
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
      "token": "string",
      "valid": "string",
      "validUntil": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string | Authentication token returned by Timewax. |
| `valid` | string | Token request validity indicator. |
| `validUntil` | date | Token expiration timestamp. |

## Native endpoint

Through the native Timewax API, this operation is `POST authentication/token/get/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authentication-token.md) for the provider-specific parameters and requirements.

