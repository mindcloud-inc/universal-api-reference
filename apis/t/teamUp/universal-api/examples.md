# TeamUp Universal API Examples

These examples use the MindCloud API key and TeamUp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Calendar Configuration

Retrieves configuration for a TeamUp calendar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-calendar-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-calendar-configuration?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "configuration": {
        "identity": {
          "title": "string"
        },
        "link": {
          "key": "https://example.com"
        },
        "subcalendars": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Calendar Configuration action reference](actions/get-calendar-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamUp/latest/actions/get-calendar-configuration).

## Create Event

Creates a new event in TeamUp.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subcalendarIds[]": [
    1
  ],
  "startDt": "string",
  "endDt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subcalendarIds[]": [1],
    "startDt": "string",
    "endDt": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "event": {
        "endDt": "string",
        "id": "string",
        "startDt": "string",
        "subcalendarIds": [
          [
            1
          ]
        ],
        "title": "string"
      },
      "undoId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Event action reference](actions/create-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamUp/latest/actions/create-event).
