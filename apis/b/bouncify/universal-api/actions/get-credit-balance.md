# Bouncify: Get Credit Balance

Retrieves credit balance information from Bouncify.

```
GET https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/get-credit-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bouncify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/get-credit-balance?${params}`, {
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
      "creditsInfo": {
        "creditsRemaining": 1,
        "paygCredit": 1,
        "subscriptionCredit": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsInfo.creditsRemaining` | number | Remaining credits across the account. |
| `creditsInfo.paygCredit` | number | Remaining pay-as-you-go credits. |
| `creditsInfo.subscriptionCredit` | number | Remaining subscription credits. |
| `success` | boolean | Whether the balance lookup succeeded. |

## Native endpoint

Through the native Bouncify API, this operation is `GET /info` (base URL `https://api.bouncify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credit-balance.md) for the provider-specific parameters and requirements.

