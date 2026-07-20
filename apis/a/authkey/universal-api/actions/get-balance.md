# Authkey: Get Balance

Retrieves the current account balance from Authkey.

```
GET https://connect.mindcloud.co/v1/universal/authkey/latest/actions/get-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Authkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/authkey/latest/actions/get-balance?${params}`, {
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
      "balance": 1,
      "currency": "string",
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `currency` | string |  |
| `email` | string |  |

## Native endpoint

Through the native Authkey API, this operation is `GET /getbalance.php` (base URL `https://console.authkey.io/restapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance.md) for the provider-specific parameters and requirements.

