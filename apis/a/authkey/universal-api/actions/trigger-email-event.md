# Authkey: Trigger Email Event

Triggers an email event in Authkey.

```
POST https://connect.mindcloud.co/v1/universal/authkey/latest/actions/trigger-email-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Authkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/authkey/latest/actions/trigger-email-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "apps@mindcloud.co",
  "mobile": "9999999999",
  "countryCode": "91",
  "eventId": "1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/authkey/latest/actions/trigger-email-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "apps@mindcloud.co",
    "mobile": "9999999999",
    "countryCode": "91",
    "eventId": "1001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Recipient email address. Example: `apps@mindcloud.co`. |
| `mobile` | string | yes | Recipient mobile number used by the event. Example: `9999999999`. |
| `countryCode` | string | yes | Recipient country dialing code. Example: `91`. |
| `eventId` | string | yes | Authkey event ID. Example: `1001`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Authkey API returns.

## Native endpoint

Through the native Authkey API, this operation is `GET https://api.authkey.io/request` (base URL `https://console.authkey.io/restapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-email-event.md) for the provider-specific parameters and requirements.

