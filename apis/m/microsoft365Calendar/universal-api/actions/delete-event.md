# Microsoft 365 Calendar: Delete Event

Deletes an existing event from Microsoft 365 Calendar.

```
DELETE https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/delete-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/delete-event?connectionId=$CONNECTION_ID&eventId=AAMkAG..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "AAMkAG..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/delete-event?${params}`, {
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
| `eventId` | string | yes | The ID of the Outlook event to delete. Example: `AAMkAG...`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 Calendar API returns.

## Native endpoint

Through the native Microsoft 365 Calendar API, this operation is `DELETE /v1.0/me/events/{{eventId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event.md) for the provider-specific parameters and requirements.

