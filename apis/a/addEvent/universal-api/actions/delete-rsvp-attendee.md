# AddEvent: Delete RSVP attendee



```
DELETE https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/delete-rsvp-attendee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/delete-rsvp-attendee?connectionId=$CONNECTION_ID&attendeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attendeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/delete-rsvp-attendee?${params}`, {
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
| `attendeeId` | string | yes | Unique identifier for the RSVP attendee. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AddEvent API returns.

## Native endpoint

Through the native AddEvent API, this operation is `DELETE /rsvps/:attendee_id` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-rsvp-attendee.md) for the provider-specific parameters and requirements.

