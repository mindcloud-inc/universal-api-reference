# ProProfs Project: Create Event

Creates a new event in ProProfs Project.

```
POST https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dueDate": "string",
  "eventName": "Ava Chen",
  "startDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dueDate": "string",
    "eventName": "Ava Chen",
    "startDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dueDate` | string | yes | The event due date in yyyymmdd format. |
| `eventName` | string | yes | The event name. |
| `projectId` | string | no | Attach the event to a project. |
| `startDate` | string | yes | The event start date in yyyymmdd format. |

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

Through the native ProProfs Project API, this operation is `POST /events` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

