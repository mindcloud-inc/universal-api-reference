# Mobile Text Alerts: Create Subscriber

Creates a new subscriber in Mobile Text Alerts.

```
POST https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/create-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mobile Text Alerts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/create-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/create-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Subscriber email address. |
| `number` | string | no | Subscriber phone number. |
| `firstName` | string | no | Subscriber first name. |
| `lastName` | string | no | Subscriber last name. |
| `groupIds` | string | no | Comma-separated Mobile Text Alerts group IDs. |
| `welcomeMessage` | string | no | Optional welcome message to send after opt-in. |

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
| `data` | object | Created or updated subscriber returned by Mobile Text Alerts. |
| `message` | string | Human-readable create result. |

## Native endpoint

Through the native Mobile Text Alerts API, this operation is `POST /subscribers` (base URL `https://api.mobile-text-alerts.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscriber.md) for the provider-specific parameters and requirements.

