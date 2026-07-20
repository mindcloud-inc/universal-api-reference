# ImageRouter: Get Credit Usage By API Key



```
GET https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/get-credit-usage-by-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageRouter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/get-credit-usage-by-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/get-credit-usage-by-api-key?${params}`, {
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
      "credit_usage": "string",
      "remaining_credits": "string",
      "total_deposits": "string",
      "usage_by_api_key": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credit_usage` | string | Total credit usage. |
| `remaining_credits` | string | Remaining account credits. |
| `total_deposits` | string | Total completed deposits. |
| `usage_by_api_key[]` | array<object> | Credit usage breakdown by API key. |
| `usage_by_api_key[].api_key_id` | string | API key identifier. |
| `usage_by_api_key[].api_key_name` | string | API key name. |
| `usage_by_api_key[].created_at` | date | API key creation timestamp when available. |
| `usage_by_api_key[].credit_usage` | string | Credit usage for the API key. |
| `usage_by_api_key[].is_active` | boolean | Whether the API key is active. |
| `usage_by_api_key[].total_requests` | number | Total requests for the API key. |

## Native endpoint

Through the native ImageRouter API, this operation is `GET /v1/credits` (base URL `https://api.imagerouter.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credit-usage-by-api-key.md) for the provider-specific parameters and requirements.

