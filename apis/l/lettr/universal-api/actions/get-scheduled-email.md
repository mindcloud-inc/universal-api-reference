# Lettr: Get Scheduled Email



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-scheduled-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-scheduled-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-scheduled-email?${params}`, {
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
| `transmissionId` | string | no | Scheduled transmission identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "events": [
          {}
        ],
        "from": "string",
        "from_name": "Ava Chen",
        "num_recipients": 1,
        "recipients": [
          "string"
        ],
        "scheduled_at": "2026-05-07T12:00:00.000Z",
        "state": "string",
        "subject": "string",
        "transmission_id": "string"
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
| `data` | object | Scheduled transmission payload. |
| `data.events` | array<object> | Delivery events when the scheduled transmission has already been processed. |
| `data.from` | string | Sender email address. |
| `data.from_name` | string | Sender display name when present. |
| `data.num_recipients` | number | Recipient count. |
| `data.recipients` | array<string> | Recipient email addresses. |
| `data.scheduled_at` | date | Scheduled send timestamp. |
| `data.state` | string | Transmission state. |
| `data.subject` | string | Email subject. |
| `data.transmission_id` | string | Scheduled transmission ID. |
| `message` | string | Scheduled email detail status message. |

## Native endpoint

Through the native Lettr API, this operation is `GET /emails/scheduled/:transmissionId` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scheduled-email.md) for the provider-specific parameters and requirements.

