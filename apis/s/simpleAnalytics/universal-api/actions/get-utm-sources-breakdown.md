# Simple Analytics: Get UTM Sources Breakdown

Retrieves a UTM source breakdown from Simple Analytics.

```
GET https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/get-utm-sources-breakdown
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simple Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/get-utm-sources-breakdown?connectionId=$CONNECTION_ID&hostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/get-utm-sources-breakdown?${params}`, {
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
| `hostname` | string | yes |  |
| `start` | string | no |  |
| `end` | string | no |  |
| `timezone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": "string",
      "end": "string",
      "generated_in_ms": 1,
      "hostname": "Ava Chen",
      "info": true,
      "ok": true,
      "path": "string",
      "start": "string",
      "timezone": "string",
      "url": "https://example.com",
      "utm_sources": [
        {}
      ],
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | string | Documentation URL returned by the API. |
| `end` | string | End timestamp for the requested reporting window. |
| `generated_in_ms` | number | Server-side generation time in milliseconds. |
| `hostname` | string | Hostname queried for analytics. |
| `info` | boolean | Whether informational fields are included. |
| `ok` | boolean | Whether the UTM sources breakdown response is valid. |
| `path` | string | Path segment covered by the report. |
| `start` | string | Start timestamp for the requested reporting window. |
| `timezone` | string | Timezone applied to the report. |
| `url` | string | Canonical website URL. |
| `utm_sources` | array<object> | Top UTM sources with aggregated pageviews and visitors. |
| `version` | number | Simple Analytics API version used for the response. |

## Native endpoint

Through the native Simple Analytics API, this operation is `GET /{{hostname}}.json` (base URL `https://simpleanalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-utm-sources-breakdown.md) for the provider-specific parameters and requirements.

