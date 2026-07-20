# ProProfs Project: Get Event

Retrieves an event from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | The event ID to fetch. |

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

Through the native ProProfs Project API, this operation is `GET /events/{{event_id}}` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

