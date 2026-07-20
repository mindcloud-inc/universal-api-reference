# TeamUp: Delete Event

Deletes an existing event from TeamUp.

```
DELETE https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/delete-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/delete-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/delete-event?${params}`, {
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
| `eventId` | string | yes | The TeamUp event identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "undoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `undoId` | string |  |

## Native endpoint

Through the native TeamUp API, this operation is `DELETE /:calendarKeyOrId/events/:eventId` (base URL `https://api.teamup.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event.md) for the provider-specific parameters and requirements.

