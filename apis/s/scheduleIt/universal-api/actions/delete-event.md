# Schedule It: Delete Event

Deletes an existing event from Schedule It.

```
DELETE https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/delete-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schedule It `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/delete-event?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/delete-event?${params}`, {
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
| `id` | number | yes | The event ID. |

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

Through the native Schedule It API, this operation is `DELETE /events/:id` (base URL `https://www.scheduleit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event.md) for the provider-specific parameters and requirements.

