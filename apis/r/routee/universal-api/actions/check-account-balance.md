# Routee: Check Account Balance

Retrieves your current Routee account balance.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-account-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-account-balance?${params}`, {
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
      "currency": {
        "code": "string",
        "name": "Ava Chen",
        "sign": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `currency` | object |  |
| `currency.code` | string |  |
| `currency.name` | string |  |
| `currency.sign` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /accounts/me/balance` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-account-balance.md) for the provider-specific parameters and requirements.

