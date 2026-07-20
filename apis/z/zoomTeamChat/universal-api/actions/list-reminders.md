# Zoom Team Chat: List Reminders



```
GET https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-reminders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/list-reminders?${params}`, {
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
| `toContact` | string | no | The contact email address for reminders. |
| `toChannel` | string | no | The channel ID for reminders. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message_id": "string",
      "to_channel": "string",
      "to_contact": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message_id` | string |  |
| `to_channel` | string |  |
| `to_contact` | string |  |

## Native endpoint

Through the native Zoom Team Chat API, this operation is `GET /chat/reminder` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reminders.md) for the provider-specific parameters and requirements.

