# Umami: Get Event Series



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-series?connectionId=$CONNECTION_ID&websiteId=string&startAt=1&endAt=1&timezone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "startAt": "1",
  "endAt": "1",
  "timezone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-event-series?${params}`, {
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
| `unit` | string | no | Time bucket unit. One of: `0`, `1`, `2`, `3`. |
| `timezone` | string | yes | Timezone like America/Los_Angeles. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "t": "2026-05-07T12:00:00.000Z",
      "x": "string",
      "y": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `t` | date | Bucket timestamp. |
| `x` | string | Event name. |
| `y` | number | Event count. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/events/series` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-series.md) for the provider-specific parameters and requirements.

