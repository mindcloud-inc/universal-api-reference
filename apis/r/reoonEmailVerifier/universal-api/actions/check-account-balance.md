# Reoon Email Verifier: Check Account Balance



```
GET https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/check-account-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reoon Email Verifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/check-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/check-account-balance?${params}`, {
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
      "api_status": "string",
      "remaining_daily_credits": 1,
      "remaining_instant_credits": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_status` | string |  |
| `remaining_daily_credits` | number |  |
| `remaining_instant_credits` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Reoon Email Verifier API, this operation is `GET /check-account-balance/` (base URL `https://emailverifier.reoon.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-account-balance.md) for the provider-specific parameters and requirements.

