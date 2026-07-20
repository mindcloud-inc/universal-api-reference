# Wooxy: Fire Event

Fires a custom event in Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/fire-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/fire-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "sender.example.com",
  "customEvent": "Stage3PurchaseUpdated20260408",
  "contact": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/fire-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "sender.example.com",
    "customEvent": "Stage3PurchaseUpdated20260408",
    "contact": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | The verified sender domain name from your Wooxy account. Example: `sender.example.com`. |
| `customEvent` | string | yes | The Wooxy event ID or event name to fire. Example: `Stage3PurchaseUpdated20260408`. |
| `contact` | string | yes | The recipient email, user ID, or phone number already stored in the default contact list. Example: `apps@mindcloud.co`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateTime` | string | no | Optional event occurrence time in ISO8601 format. Example: `2026-04-08T17:00:00+00:00`. |
| `ipAddress` | string | no | Optional IPv4 address associated with the event. Example: `127.0.0.1`. |
| `userAgent` | string | no | Optional user agent string. Example: `Mozilla/5.0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/custom-event/fire` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fire-event.md) for the provider-specific parameters and requirements.

