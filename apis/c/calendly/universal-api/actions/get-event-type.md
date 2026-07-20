# Calendly: Get Event Type

Retrieves an event type from Calendly.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/get-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/get-event-type?connectionId=$CONNECTION_ID&event_type_uuid=8d38b11a-269e-4878-ab4a-12048b63906d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event_type_uuid": "8d38b11a-269e-4878-ab4a-12048b63906d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/get-event-type?${params}`, {
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
| `event_type_uuid` | string | yes | Event type UUID from Calendly. Default: `8d38b11a-269e-4878-ab4a-12048b63906d`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Calendly API returns.

## Native endpoint

Through the native Calendly API, this operation is `GET /event_types/:event_type_uuid` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-type.md) for the provider-specific parameters and requirements.

