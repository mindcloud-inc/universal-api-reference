# Maildrip: Get top-up rate



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-top-up-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-top-up-rate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-top-up-rate?${params}`, {
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
      "topupInDollar": 1,
      "topupInNaira": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `topupInDollar` | number | Top-up rate in dollars |
| `topupInNaira` | number | Top-up rate in naira |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/payment/paystack/transactions/topup` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-top-up-rate.md) for the provider-specific parameters and requirements.

