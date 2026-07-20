# Peggy Pay: Authorize API Key

Retrieves an access token from Peggy Pay.

```
GET https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/authorize-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peggy Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/authorize-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/authorize-api-key?${params}`, {
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
      "Token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Token` | string | Peggy Pay session token returned by Framework.authorize. |

## Native endpoint

Through the native Peggy Pay API, this operation is `GET Framework.authorize` (base URL `https://www.peggypay.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authorize-api-key.md) for the provider-specific parameters and requirements.

