# Simple Analytics: Get Event Counts

Retrieves specified event counts from Simple Analytics.

```
GET https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/get-event-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simple Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/get-event-counts?connectionId=$CONNECTION_ID&hostname=Ava%20Chen&events=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostname": "Ava Chen",
  "events": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/get-event-counts?${params}`, {
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
| `hostname` | string | yes | Website hostname to query, for example `simpleanalytics.com`. |
| `start` | string | no | Start date or placeholder such as `yesterday`. |
| `end` | string | no | End date or placeholder such as `today`. |
| `timezone` | string | no | IANA time zone such as `Europe/Amsterdam`. |
| `events` | string | yes | Comma-separated event names, or `*` for all events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": "string",
      "end": "string",
      "events": [
        {}
      ],
      "generated_in_ms": 1,
      "hostname": "Ava Chen",
      "info": true,
      "ok": true,
      "path": "string",
      "start": "string",
      "timezone": "string",
      "url": "https://example.com",
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
| `events` | array<object> | Event totals returned for the requested selector. |
| `generated_in_ms` | number | Server-side generation time in milliseconds. |
| `hostname` | string | Hostname queried for analytics. |
| `info` | boolean | Whether informational fields are included. |
| `ok` | boolean | Whether the event report response is valid. |
| `path` | string | Path segment covered by the report. |
| `start` | string | Start timestamp for the requested reporting window. |
| `timezone` | string | Timezone applied to the report. |
| `url` | string | Canonical website URL. |
| `version` | number | Simple Analytics API version used for the response. |

## Native endpoint

Through the native Simple Analytics API, this operation is `GET /{{hostname}}.json` (base URL `https://simpleanalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-counts.md) for the provider-specific parameters and requirements.

