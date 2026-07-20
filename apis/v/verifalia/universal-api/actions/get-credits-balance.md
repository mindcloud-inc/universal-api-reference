# Verifalia: Get Credits Balance

Retrieves the current credits balance from Verifalia.

```
GET https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-credits-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-credits-balance?${params}`, {
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
      "creditPacks": 1,
      "freeCredits": 1,
      "freeCreditsResetIn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditPacks` | number | Remaining purchased Verifalia credits. |
| `freeCredits` | number | Remaining free credits for the current reset window. |
| `freeCreditsResetIn` | string | Time remaining before free credits reset, expressed by Verifalia as a duration string. |

## Native endpoint

Through the native Verifalia API, this operation is `GET /credits/balance` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits-balance.md) for the provider-specific parameters and requirements.

