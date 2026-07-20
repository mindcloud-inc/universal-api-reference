# Statsig: Get metrics using event name

Retrieves metrics from Statsig by event name.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-metrics-using-event-name-get-console-v1-events-eventname-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-metrics-using-event-name-get-console-v1-events-eventname-metrics?connectionId=$CONNECTION_ID&limit=25&offset=0&eventName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "eventName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-metrics-using-event-name-get-console-v1-events-eventname-metrics?${params}`, {
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
| `eventName` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Results per page |
| `page` | number | no | Page number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/events/{eventName}/metrics` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-metrics-using-event-name-get-console-v1-events-eventname-metrics.md) for the provider-specific parameters and requirements.

