# Morf: Send Track Event

Sends a track event to Morf.

```
POST https://connect.mindcloud.co/v1/universal/morf/latest/actions/send-track-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/morf/latest/actions/send-track-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_name": "Ava Chen",
  "user_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morf/latest/actions/send-track-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_name": "Ava Chen",
    "user_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event_name` | string | yes | Name of the Track event to send to Morf. |
| `user_id` | string | yes | Unique user ID for the Track event. Morf stores this as the active customer ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event_id` | string | no | Optional unique identifier for the Track event. |
| `occurred_at` | date | no | Optional event time in RFC3339 ISO format. |
| `profile_ids` | object | no | Optional third-party IDs to associate with the Morf Profile. |
| `profile_properties` | object | no | Optional property values to store on the Morf Profile. |
| `event_data` | object | no | Optional data associated with the event for Morf Workflows. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status_code` | number | Morf Track processing status code returned by the Track endpoint. |

## Native endpoint

Through the native Morf API, this operation is `POST` (base URL `{{credentials.trackWebhookUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-track-event.md) for the provider-specific parameters and requirements.

