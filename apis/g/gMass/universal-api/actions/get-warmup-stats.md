# GMass: Get Warmup Stats

Retrieves warmup stats for your GMass account.

```
GET https://connect.mindcloud.co/v1/universal/gMass/latest/actions/get-warmup-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/get-warmup-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/get-warmup-stats?${params}`, {
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
      "Date": "2026-05-07T12:00:00.000Z",
      "Inbox": 1,
      "Missing": 1,
      "Promotions": 1,
      "Spam": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Date` | date | Warm-up reporting date. |
| `Inbox` | number | Messages that landed in inbox. |
| `Missing` | number | Messages that are missing from tracked folders. |
| `Promotions` | number | Messages that landed in promotions. |
| `Spam` | number | Messages that landed in spam. |

## Native endpoint

Through the native GMass API, this operation is `GET /user/WarmupStats` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-warmup-stats.md) for the provider-specific parameters and requirements.

