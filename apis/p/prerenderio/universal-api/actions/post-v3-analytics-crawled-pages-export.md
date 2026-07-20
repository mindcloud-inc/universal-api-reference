# Prerender.io: Create Analytics Crawled Pages Export

Creates an analytics crawled pages export in Prerender.io.

```
POST https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-analytics-crawled-pages-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-analytics-crawled-pages-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cache_hit": 1,
  "crawlers": "string",
  "date_from": "string",
  "date_to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/post-v3-analytics-crawled-pages-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cache_hit": 1,
    "crawlers": "string",
    "date_from": "string",
    "date_to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adaptive_type` | string | no |  |
| `cache_hit` | list<number> | yes |  |
| `crawlers` | list<string> | yes |  |
| `date_from` | string | yes |  |
| `date_to` | string | yes |  |
| `domain` | string | no |  |
| `q` | string | no |  |
| `q_condition` | string | no |  |
| `response_time_high` | number | no |  |
| `response_time_low` | number | no |  |
| `sort` | string | no |  |
| `sort_direction` | string | no |  |
| `status_code` | number | no |  |
| `status_code_high` | number | no |  |
| `status_code_low` | number | no |  |
| `timedout` | boolean | no |  |
| `timezone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object |  |

## Native endpoint

Through the native Prerender.io API, this operation is `POST /v3/analytics/crawled-pages/export` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-v3-analytics-crawled-pages-export.md) for the provider-specific parameters and requirements.

