# ProProfs Project: Update Event

Updates an existing event in ProProfs Project.

```
PUT https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/update-event', {
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
| `dueDate` | string | no | The updated event due date in yyyymmdd format. |
| `eventId` | string | yes | The event ID to update. |
| `eventName` | string | no | The updated event name. |
| `projectId` | string | no | Attach the updated event to a project. |
| `startDate` | string | no | The updated event start date in yyyymmdd format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "string",
      "dateModified": "string",
      "dueDate": "string",
      "eventId": "string",
      "eventName": "Ava Chen",
      "projectId": "string",
      "startDate": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `dueDate` | string |  |
| `eventId` | string |  |
| `eventName` | string |  |
| `projectId` | string |  |
| `startDate` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `PUT /events/{{event_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

