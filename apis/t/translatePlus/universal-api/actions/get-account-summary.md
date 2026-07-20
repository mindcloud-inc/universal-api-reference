# TranslatePlus: Get Account Summary

Retrieves account summary and credit usage from TranslatePlus.

```
GET https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/get-account-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TranslatePlus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/get-account-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/get-account-summary?${params}`, {
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
      "concurrency": 1,
      "credits_percentage": 1,
      "credits_remaining": 1,
      "credits_used": 1,
      "effective_concurrency": 1,
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "summary": {},
      "total_credits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `concurrency` | number |  |
| `credits_percentage` | number |  |
| `credits_remaining` | number |  |
| `credits_used` | number |  |
| `effective_concurrency` | number |  |
| `email` | string |  |
| `full_name` | string |  |
| `summary` | object |  |
| `total_credits` | number |  |

## Native endpoint

Through the native TranslatePlus API, this operation is `GET /v2/account/summary` (base URL `https://api.translateplus.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-summary.md) for the provider-specific parameters and requirements.

