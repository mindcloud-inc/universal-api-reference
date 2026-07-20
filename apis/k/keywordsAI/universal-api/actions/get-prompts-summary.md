# Keywords AI: Get Prompts Summary

Retrieves prompt summary statistics from Keywords AI.

```
GET https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/get-prompts-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keywords AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/get-prompts-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/get-prompts-summary?${params}`, {
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
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total_count` | number |  |

## Native endpoint

Through the native Keywords AI API, this operation is `GET /api/prompts/summary/` (base URL `https://api.respan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prompts-summary.md) for the provider-specific parameters and requirements.

