# MailoPost: Get Balance

Retrieves account balance details from MailoPost.

```
GET https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-balance?${params}`, {
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
      "tariff": {
        "credits": 1,
        "expires_at": 1,
        "subscribers": {
          "available": 1,
          "total": 1
        }
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
| `tariff.credits` | number |  |
| `tariff.expires_at` | number |  |
| `tariff.subscribers.available` | number |  |
| `tariff.subscribers.total` | number |  |

## Native endpoint

Through the native MailoPost API, this operation is `GET /email/balance` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance.md) for the provider-specific parameters and requirements.

