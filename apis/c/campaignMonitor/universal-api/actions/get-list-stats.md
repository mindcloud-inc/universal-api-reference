# Campaign Monitor: Get List Stats

Retrieves statistics for a Campaign Monitor list.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-list-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-list-stats?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-list-stats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Campaign Monitor list identifier. |

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
| `bouncesThisMonth` | number | Bounces recorded this month. |
| `bouncesThisWeek` | number | Bounces recorded this week. |
| `bouncesThisYear` | number | Bounces recorded this year. |
| `bouncesToday` | number | Bounces recorded today. |
| `bouncesYesterday` | number | Bounces recorded yesterday. |
| `deletedThisMonth` | number | Deleted subscribers recorded this month. |
| `deletedThisWeek` | number | Deleted subscribers recorded this week. |
| `deletedThisYear` | number | Deleted subscribers recorded this year. |
| `deletedToday` | number | Deleted subscribers recorded today. |
| `deletedYesterday` | number | Deleted subscribers recorded yesterday. |
| `newActiveSubscribersThisMonth` | number | New active subscribers added this month. |
| `newActiveSubscribersThisWeek` | number | New active subscribers added this week. |
| `newActiveSubscribersThisYear` | number | New active subscribers added this year. |
| `newActiveSubscribersToday` | number | New active subscribers added today. |
| `newActiveSubscribersYesterday` | number | New active subscribers added yesterday. |
| `totalActiveSubscribers` | number | Total active subscribers in the list. |
| `totalBounces` | number | Total bounced subscribers for the list. |
| `totalDeleted` | number | Total deleted subscribers for the list. |
| `totalUnsubscribes` | number | Total unsubscribes for the list. |
| `unsubscribesThisMonth` | number | Unsubscribes recorded this month. |
| `unsubscribesThisWeek` | number | Unsubscribes recorded this week. |
| `unsubscribesThisYear` | number | Unsubscribes recorded this year. |
| `unsubscribesToday` | number | Unsubscribes recorded today. |
| `unsubscribesYesterday` | number | Unsubscribes recorded yesterday. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /lists/:listId/stats.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-stats.md) for the provider-specific parameters and requirements.

