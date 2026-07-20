# Umami: Get Event Stats



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-stats?connectionId=$CONNECTION_ID&websiteId=string&startAt=1&endAt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "startAt": "1",
  "endAt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-stats?${params}`, {
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
| `websiteId` | string | yes | The website ID. |
| `startAt` | number | yes | Start timestamp in milliseconds. |
| `endAt` | number | yes | End timestamp in milliseconds. |
| `compare` | string | no | Comparison period. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comparison": {},
      "events": 1,
      "uniqueEvents": 1,
      "visitors": 1,
      "visits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comparison` | object | Comparison totals for the previous comparison window. |
| `events` | number | Total events in the selected range. |
| `uniqueEvents` | number | Count of unique event names. |
| `visitors` | number | Total visitors who triggered events. |
| `visits` | number | Total visits with events. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/events/stats` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-stats.md) for the provider-specific parameters and requirements.

