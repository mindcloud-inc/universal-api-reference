# Zoho Calendar: Create Event Using Smart Add

Creates a new event in Zoho Calendar using Smart Add.

```
POST https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-event-using-smart-add
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-event-using-smart-add" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/create-event-using-smart-add', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Natural-language Smart Add text to turn into an event. Zoho currently expects this query value as saddtext at runtime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "dateandtime": {
            "end": "string",
            "start": "string",
            "timezone": "string"
          },
          "description": "string",
          "isallday": true,
          "isprivate": true,
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[].dateandtime.end` | string |  |
| `events[].dateandtime.start` | string |  |
| `events[].dateandtime.timezone` | string |  |
| `events[].description` | string |  |
| `events[].isallday` | boolean |  |
| `events[].isprivate` | boolean |  |
| `events[].title` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `POST /smartadd` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-using-smart-add.md) for the provider-specific parameters and requirements.

