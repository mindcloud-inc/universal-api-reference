# Dynosend: Send Contact Event by UID

Creates an event in Dynosend for a contact UID.

```
POST https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/send-contact-event-by-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/send-contact-event-by-uid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audienceUid": "string",
  "contactUid": "string",
  "eventName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/send-contact-event-by-uid', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audienceUid": "string",
    "contactUid": "string",
    "eventName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audienceUid` | string | yes | The UID of the audience that contains the contact. |
| `contactUid` | string | yes | The UID of the contact the event belongs to. |
| `eventName` | string | yes | The event name to send. Use only letters, numbers, and underscores. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dynosend API returns.

## Native endpoint

Through the native Dynosend API, this operation is `POST /events` (base URL `https://api.dynosend.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-contact-event-by-uid.md) for the provider-specific parameters and requirements.

