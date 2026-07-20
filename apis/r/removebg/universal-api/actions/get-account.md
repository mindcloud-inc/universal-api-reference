# Remove.bg: Get Account

Retrieves account credit balances from Remove.bg.

```
GET https://connect.mindcloud.co/v1/universal/removebg/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remove.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/removebg/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/removebg/latest/actions/get-account?${params}`, {
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
      "api": {
        "freeCalls": 1,
        "sizes": "string"
      },
      "credits": {
        "enterprise": 1,
        "payg": 1,
        "subscription": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api.freeCalls` | number |  |
| `api.sizes` | string |  |
| `credits.enterprise` | number |  |
| `credits.payg` | number |  |
| `credits.subscription` | number |  |
| `credits.total` | number |  |

## Native endpoint

Through the native Remove.bg API, this operation is `GET /account` (base URL `https://api.remove.bg/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

