# Vyte: Retrieve Event

Retrieves an event from Vyte.

```
GET https://connect.mindcloud.co/v1/universal/vyte/latest/actions/retrieve-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/retrieve-event?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vyte/latest/actions/retrieve-event?${params}`, {
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
| `eventId` | string | no | The Vyte event ID. Default: `69cab3650e9b6ae2ac784c91`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "first_start_date": "string",
      "invitees_length": 1,
      "last_end_date": "string",
      "org": "string",
      "timezone": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `first_start_date` | string |  |
| `invitees_length` | number |  |
| `last_end_date` | string |  |
| `org` | string |  |
| `timezone` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Vyte API, this operation is `GET v2/events/:event_id` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-event.md) for the provider-specific parameters and requirements.

