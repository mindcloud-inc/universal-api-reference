# Scrape do: Get usage statistics

Retrieves usage statistics from Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-usage-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-usage-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-usage-statistics?${params}`, {
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
      "ConcurrentRequest": 1,
      "IsActive": true,
      "MaxMonthlyRequest": 1,
      "RemainingConcurrentRequest": 1,
      "RemainingMonthlyRequest": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ConcurrentRequest` | number | Total allowed concurrency. |
| `IsActive` | boolean | Whether the account is active. |
| `MaxMonthlyRequest` | number | Monthly request limit. |
| `RemainingConcurrentRequest` | number | Remaining concurrency slots. |
| `RemainingMonthlyRequest` | number | Remaining monthly requests. |

## Native endpoint

Through the native Scrape do API, this operation is `GET /info` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-statistics.md) for the provider-specific parameters and requirements.

