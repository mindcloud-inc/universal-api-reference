# Enrich.so: Get Credit Balance

Retrieves credit balance from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-credit-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-credit-balance?${params}`, {
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
      "credits_remaining": 1,
      "credits_used": 1,
      "team": "string",
      "total_credits": 1,
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number | Credits remaining for the team. |
| `credits_used` | number | Credits already consumed. |
| `team` | string | Authenticated Enrich team name. |
| `total_credits` | number | Total credits available to the team. |
| `uid` | string | Authenticated Enrich team identifier. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /wallets/balance` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credit-balance.md) for the provider-specific parameters and requirements.

