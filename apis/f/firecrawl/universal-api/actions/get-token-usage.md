# Firecrawl: Get Token Usage

Retrieves token usage from Firecrawl.

```
GET https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-token-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-token-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-token-usage?${params}`, {
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
      "billingPeriodEnd": "2026-05-07T12:00:00.000Z",
      "billingPeriodStart": "2026-05-07T12:00:00.000Z",
      "planTokens": 1,
      "remainingTokens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingPeriodEnd` | date |  |
| `billingPeriodStart` | date |  |
| `planTokens` | number |  |
| `remainingTokens` | number |  |

## Native endpoint

Through the native Firecrawl API, this operation is `GET /team/token-usage` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-usage.md) for the provider-specific parameters and requirements.

