# Schedule It: Update Event

Updates an existing event in Schedule It.

```
PUT https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schedule It `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The event ID. |
| `title` | string | no | The updated event title. |
| `notes` | string | no | Updated notes for the event. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color_back": "string",
      "color_text": "string",
      "completed": "string",
      "date_end": "string",
      "date_start": "string",
      "geonav": "string",
      "id": "string",
      "location": "string",
      "locked": "string",
      "notes": "string",
      "owner": "string",
      "owner_names_simple": "Ava Chen",
      "parentid": "string",
      "priority": "string",
      "private": "string",
      "starticon": "string",
      "style": "string",
      "title": "string",
      "workingduration": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color_back` | string |  |
| `color_text` | string |  |
| `completed` | string |  |
| `date_end` | string |  |
| `date_start` | string |  |
| `geonav` | string |  |
| `id` | string |  |
| `location` | string |  |
| `locked` | string |  |
| `notes` | string |  |
| `owner` | string |  |
| `owner_names_simple` | string |  |
| `parentid` | string |  |
| `priority` | string |  |
| `private` | string |  |
| `starticon` | string |  |
| `style` | string |  |
| `title` | string |  |
| `workingduration` | string |  |

## Native endpoint

Through the native Schedule It API, this operation is `POST /events/:id` (base URL `https://www.scheduleit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

