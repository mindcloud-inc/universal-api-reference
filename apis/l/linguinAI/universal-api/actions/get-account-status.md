# Linguin AI: Get Account Status



```
GET https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/get-account-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linguin AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/get-account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/get-account-status?${params}`, {
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
      "daily_limit": 1,
      "detections_today": 1,
      "remaining_today": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `daily_limit` | number | The daily detection limit for the account. |
| `detections_today` | number | How many detections the account has used today. |
| `remaining_today` | number | How many detections remain today. |

## Native endpoint

Through the native Linguin AI API, this operation is `GET /v2/status` (base URL `https://api.linguin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-status.md) for the provider-specific parameters and requirements.

