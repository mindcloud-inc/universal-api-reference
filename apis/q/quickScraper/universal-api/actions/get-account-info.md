# Quick Scraper: Get Account Info

Retrieves account details from Quick Scraper.

```
GET https://connect.mindcloud.co/v1/universal/quickScraper/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quick Scraper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickScraper/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickScraper/latest/actions/get-account-info?${params}`, {
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
      "allocatedCredits": 1,
      "allowedConcurrentRequests": 1,
      "currentConcurrentRequests": 1,
      "failedRequests": 1,
      "remainingCredits": 1,
      "subscriptionExpiryDate": "2026-05-07T12:00:00.000Z",
      "successRequests": 1,
      "usedCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocatedCredits` | number | Monthly credit allocation for the current Quick Scraper account. |
| `allowedConcurrentRequests` | number | Maximum concurrent requests allowed for the account. |
| `currentConcurrentRequests` | number | Concurrent requests currently in use. |
| `failedRequests` | number | Failed requests recorded for the current period. |
| `remainingCredits` | number | Credits still available in the current period. |
| `subscriptionExpiryDate` | date | Subscription expiry timestamp returned by Quick Scraper. |
| `successRequests` | number | Successful requests recorded for the current period. |
| `usedCredits` | number | Credits already consumed in the current period. |

## Native endpoint

Through the native Quick Scraper API, this operation is `GET /account` (base URL `https://api.quickscraper.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

