# Mobile Text Alerts: Send Message

Creates a message in Mobile Text Alerts.

```
POST https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mobile Text Alerts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscribers": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscribers": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscribers` | string | yes | Comma-separated phone numbers or emails to send the message to. |
| `message` | string | no | Message content to send. |
| `templateId` | number | no | Controlled template ID to use instead of freeform message content. |
| `image` | string | no | Optional attachment URL for MMS sends. |
| `header` | string | no | Optional text inserted before the message body. |
| `footer` | string | no | Optional text appended after the message body. |
| `scheduledDate` | string | no | Optional scheduled send time in ISO 8601 format like 20250306T193000-0000. |

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
| `data` | object | Send result payload including the new message ID and counts. |
| `message` | string | Human-readable send result. |

## Native endpoint

Through the native Mobile Text Alerts API, this operation is `POST /send` (base URL `https://api.mobile-text-alerts.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

