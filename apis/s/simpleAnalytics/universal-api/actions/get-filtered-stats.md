# Simple Analytics: Get Filtered Stats

Retrieves filtered stats from Simple Analytics.

```
GET https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/get-filtered-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simple Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/get-filtered-stats?connectionId=$CONNECTION_ID&hostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/get-filtered-stats?${params}`, {
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
| `hostname` | string | yes | Website hostname to query. |
| `start` | string | no | Start date like 2026-04-01, today, or today-30d. |
| `end` | string | no | End date like 2026-04-14, yesterday, or today. |
| `limit` | string | no | Limit returned breakdown rows between 1 and 1000. |
| `timezone` | string | no | Timezone like Europe/Amsterdam or UTC. |
| `info` | string | no | Include informational helper fields in the response. |
| `callback` | string | no | Wrap the response in a JSONP callback. |
| `events` | string | no | Comma-separated event names or * to return all events. |
| `interval` | string | no | Histogram interval: hour, day, week, month, or year. |
| `fields` | string | no | Comma-separated fields like histogram,pages,countries or seconds_on_page. |
| `page` | string | no | Filter by one page path. |
| `pages` | string | no | Filter by comma-separated page paths or wildcard patterns. |
| `country` | string | no | Filter by one country code. |
| `referrer` | string | no | Filter by one normalized referrer. |
| `utm_source` | string | no | Filter by one UTM source. |
| `utm_medium` | string | no | Filter by one UTM medium. |
| `utm_campaign` | string | no | Filter by one UTM campaign. |
| `utm_content` | string | no | Filter by one UTM content. |
| `utm_term` | string | no | Filter by one UTM term. |
| `browser_name` | string | no | Filter by one browser name. |
| `os_name` | string | no | Filter by one operating system name. |
| `device_type` | string | no | Filter by one device type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Simple Analytics API returns.

## Native endpoint

Through the native Simple Analytics API, this operation is `GET /{{hostname}}.json` (base URL `https://simpleanalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filtered-stats.md) for the provider-specific parameters and requirements.

