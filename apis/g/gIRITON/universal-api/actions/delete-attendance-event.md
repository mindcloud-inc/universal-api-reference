# GIRITON: Delete Attendance Event

Deletes an attendance event from GIRITON.

```
DELETE https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/delete-attendance-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/delete-attendance-event?connectionId=$CONNECTION_ID&attendanceEventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attendanceEventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/delete-attendance-event?${params}`, {
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
| `attendanceEventId` | string | yes | Attendance event ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GIRITON API returns.

## Native endpoint

Through the native GIRITON API, this operation is `DELETE /attendance/attendanceEvent` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-attendance-event.md) for the provider-specific parameters and requirements.

