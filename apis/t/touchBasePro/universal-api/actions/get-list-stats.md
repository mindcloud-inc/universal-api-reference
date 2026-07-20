# TouchBasePro: Get List Stats

Retrieves statistics for a list from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-list-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-list-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-list-stats?${params}`, {
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
      "bouncesThisMonth": 1,
      "bouncesThisWeek": 1,
      "bouncesThisYear": 1,
      "bouncesToday": 1,
      "bouncesYesterday": 1,
      "deletedThisMonth": 1,
      "deletedThisWeek": 1,
      "deletedThisYear": 1,
      "deletedToday": 1,
      "deletedYesterday": 1,
      "newActiveSubscribersThisMonth": 1,
      "newActiveSubscribersThisWeek": 1,
      "newActiveSubscribersThisYear": 1,
      "newActiveSubscribersToday": 1,
      "newActiveSubscribersYesterday": 1,
      "totalActiveSubscribers": 1,
      "totalBounces": 1,
      "totalDeleted": 1,
      "totalUnsubscribes": 1,
      "unsubscribesThisMonth": 1,
      "unsubscribesThisWeek": 1,
      "unsubscribesThisYear": 1,
      "unsubscribesToday": 1,
      "unsubscribesYesterday": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bouncesThisMonth` | number |  |
| `bouncesThisWeek` | number |  |
| `bouncesThisYear` | number |  |
| `bouncesToday` | number |  |
| `bouncesYesterday` | number |  |
| `deletedThisMonth` | number |  |
| `deletedThisWeek` | number |  |
| `deletedThisYear` | number |  |
| `deletedToday` | number |  |
| `deletedYesterday` | number |  |
| `newActiveSubscribersThisMonth` | number |  |
| `newActiveSubscribersThisWeek` | number |  |
| `newActiveSubscribersThisYear` | number |  |
| `newActiveSubscribersToday` | number |  |
| `newActiveSubscribersYesterday` | number |  |
| `totalActiveSubscribers` | number |  |
| `totalBounces` | number |  |
| `totalDeleted` | number |  |
| `totalUnsubscribes` | number |  |
| `unsubscribesThisMonth` | number |  |
| `unsubscribesThisWeek` | number |  |
| `unsubscribesThisYear` | number |  |
| `unsubscribesToday` | number |  |
| `unsubscribesYesterday` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/lists/{listId}/stats` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-stats.md) for the provider-specific parameters and requirements.

