# Kimi: Check Balance

Retrieves your account balance from Kimi.

```
GET https://connect.mindcloud.co/v1/universal/kimi/latest/actions/check-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kimi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kimi/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kimi/latest/actions/check-balance?${params}`, {
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
      "code": 1,
      "data": {
        "availableBalance": 1,
        "cashBalance": 1,
        "voucherBalance": 1
      },
      "scode": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Provider response code. |
| `data` | object | Balance information. |
| `data.availableBalance` | number | Available balance. |
| `data.cashBalance` | number | Cash balance. |
| `data.voucherBalance` | number | Voucher balance. |
| `scode` | string | Provider status code. |
| `status` | boolean | Whether the balance request succeeded. |

## Native endpoint

Through the native Kimi API, this operation is `GET /v1/users/me/balance` (base URL `https://api.moonshot.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-balance.md) for the provider-specific parameters and requirements.

