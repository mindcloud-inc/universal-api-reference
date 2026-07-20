# Calendly: Create Single-Use Scheduling Link

Creates a single-use scheduling link in Calendly.

```
POST https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-single-use-scheduling-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-single-use-scheduling-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d",
  "owner_type": "EventType"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendly/latest/actions/create-single-use-scheduling-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d",
    "owner_type": "EventType"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | string | yes | Owner URI (event type or user). Default: `https://api.calendly.com/event_types/8d38b11a-269e-4878-ab4a-12048b63906d`. |
| `owner_type` | string | yes | Owner type: EventType or User. Default: `EventType`. |
| `max_event_count` | number | no | Maximum times this link can be used. Default: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expires_at` | date | no | Scheduling link expiration time (ISO-8601). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Calendly API returns.

## Native endpoint

Through the native Calendly API, this operation is `POST /scheduling_links` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-single-use-scheduling-link.md) for the provider-specific parameters and requirements.

