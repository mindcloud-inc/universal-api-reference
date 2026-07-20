# Launch27: Get FSPay Token

Retrieves an FSPay token from Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-fspay-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-fspay-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-fspay-token?${params}`, {
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
      "authentication_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authentication_key` | string | FullSteam hosted-payments authentication key returned by the Launch27 payment bootstrap. |

## Native endpoint

Through the native Launch27 API, this operation is `POST fspay/token` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fspay-token.md) for the provider-specific parameters and requirements.

