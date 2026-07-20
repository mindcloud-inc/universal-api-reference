# CodeQR - Link and QR Analytics: List Events

Retrieves events from CodeQR.

```
GET https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-events?${params}`, {
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
| `event` | string | no | The type of event to retrieve. Default: `clicks`. |
| `interval` | string | no | The interval to retrieve events for. Default: `24h`. |
| `page` | number | no | The page number for events pagination. Default: `1`. |
| `limit` | number | no | The number of events to return. Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "click": {},
      "customer": {},
      "event": "string",
      "eventId": "string",
      "eventName": "Ava Chen",
      "link": {},
      "sale": {},
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `click` | object |  |
| `customer` | object |  |
| `event` | string |  |
| `eventId` | string |  |
| `eventName` | string |  |
| `link` | object |  |
| `sale` | object |  |
| `timestamp` | date |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `GET /events` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

