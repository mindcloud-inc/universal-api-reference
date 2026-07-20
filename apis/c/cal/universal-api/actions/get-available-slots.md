# Cal.com: Get Available Slots

Retrieves available slots from Cal.com.

```
GET https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-available-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-available-slots?connectionId=$CONNECTION_ID&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-available-slots?${params}`, {
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
| `bookingUidToReschedule` | list | no | Existing booking UID when requesting slots for rescheduling. |
| `duration` | number | no | Requested slot duration in minutes. |
| `eventTypeId` | list | no | Event type ID to resolve slots. |
| `eventTypeSlug` | list | no | Event type slug to resolve slots. |
| `format` | list | no | Response slot format option. One of: `range`, `time`. |
| `organizationSlug` | string | no | Organization slug for event type lookup. |
| `start` | string | yes | Range start in ISO 8601 UTC format. |
| `teamSlug` | string | no | Team slug for event type lookup. |
| `timeZone` | string | no | IANA time zone for slot rendering. |
| `username` | string | no | Username for user-scoped event type lookup. |
| `usernames` | string | no | Comma-separated usernames for team lookup. |
| `end` | string | yes | Range end in ISO 8601 UTC format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cal.com API returns.

## Native endpoint

Through the native Cal.com API, this operation is `GET /slots` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-available-slots.md) for the provider-specific parameters and requirements.

