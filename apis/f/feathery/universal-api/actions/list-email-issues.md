# Feathery: List Email Issues



```
GET https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-email-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-email-issues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-email-issues?${params}`, {
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
| `event_type` | string | no | Filter to `Bounce` or `Complaint` events. One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start_time` | date | no | Only return email events after this time. |
| `end_time` | date | no | Only return email events before this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "event_type": "string",
      "recipients": [
        "string"
      ],
      "rejected_recipients": [
        "string"
      ],
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | When the event occurred. |
| `event_type` | string | The email event type. |
| `recipients` | array<string> | The recipient addresses. |
| `rejected_recipients` | array<string> | The rejected recipient addresses. |
| `subject` | string | The email subject. |

## Native endpoint

Through the native Feathery API, this operation is `GET /api/logs/email/issues/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-issues.md) for the provider-specific parameters and requirements.

