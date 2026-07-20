# Pencil Spaces: Update Event



```
PUT https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pencil Spaces `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Updated description of the event. |
| `end` | string | no | Updated RFC3339 end timestamp for the event. |
| `eventId` | string | yes | The Pencil eventId of the event to update. |
| `organizers[]` | array<object> | no | Organizer list for the event. |
| `organizers[].userId` | string | no | Organizer userId. |
| `spaceId` | string | no | Updated Pencil spaceId associated with the event. |
| `start` | string | no | Updated RFC3339 start timestamp for the event. |
| `title` | string | no | Updated title of the event. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pencil Spaces API returns.

## Native endpoint

Through the native Pencil Spaces API, this operation is `PUT /events/:eventId` (base URL `https://apis.pencilapp.com/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

