# Lettr: Get Email Detail



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-email-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-email-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-email-detail?${params}`, {
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
| `requestId` | string | no | Email request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "events": {
          "data": {
            "event_id": "string",
            "friendly_from": "string",
            "queue_time": 1,
            "rcpt_to": "string",
            "request_id": "string",
            "subject": "string",
            "timestamp": "2026-05-07T12:00:00.000Z",
            "type": "string"
          },
          "from": "2026-05-07T12:00:00.000Z",
          "to": "2026-05-07T12:00:00.000Z",
          "total_count": 1
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Email detail payload. |
| `data.events` | object | Event collection wrapper. |
| `data.events.data` | array<object> | Events for the requested email. |
| `data.events.data.event_id` | string | Event ID. |
| `data.events.data.friendly_from` | string | Sender address. |
| `data.events.data.queue_time` | number | Queue time in milliseconds when present. |
| `data.events.data.rcpt_to` | string | Recipient email address. |
| `data.events.data.request_id` | string | Email request ID. |
| `data.events.data.subject` | string | Email subject. |
| `data.events.data.timestamp` | date | Event timestamp. |
| `data.events.data.type` | string | Event type. |
| `data.events.from` | date | Range start timestamp. |
| `data.events.to` | date | Range end timestamp. |
| `data.events.total_count` | number | Total event count. |
| `message` | string | Email detail retrieval status message. |

## Native endpoint

Through the native Lettr API, this operation is `GET /emails/:requestId` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-detail.md) for the provider-specific parameters and requirements.

