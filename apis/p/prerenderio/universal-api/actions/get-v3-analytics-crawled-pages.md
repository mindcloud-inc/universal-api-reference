# Prerender.io: List Analytics Crawled Pages

Retrieves analytics crawled pages from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-analytics-crawled-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-analytics-crawled-pages?connectionId=$CONNECTION_ID&cache_hit=1&crawlers=string&date_from=string&date_to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cache_hit": "1",
  "crawlers": "string",
  "date_from": "string",
  "date_to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-analytics-crawled-pages?${params}`, {
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
| `adaptive_type` | string | no |  |
| `cache_hit` | list<number> | yes |  |
| `crawlers` | list<string> | yes |  |
| `date_from` | string | yes |  |
| `date_to` | string | yes |  |
| `domain` | string | no |  |
| `page` | number | no |  |
| `page_size` | number | no |  |
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/analytics/crawled-pages` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-analytics-crawled-pages.md) for the provider-specific parameters and requirements.

