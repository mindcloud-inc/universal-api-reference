# Twitch Universal API Examples

These examples use the MindCloud API key and Twitch connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Channel Stream Schedule

Retrieves channel stream schedules from Twitch.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/get-channel-stream-schedule?connectionId=$CONNECTION_ID&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcasterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/get-channel-stream-schedule?${params}`, {
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
      "broadcasterId": "string",
      "broadcasterLogin": "string",
      "broadcasterName": "Ava Chen",
      "segments": [
        {
          "canceledUntil": {},
          "category": {},
          "endTime": {},
          "id": "string",
          "isRecurring": true,
          "startTime": "string",
          "title": "string"
        }
      ],
      "vacation": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Channel Stream Schedule action reference](actions/get-channel-stream-schedule.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/twitch/latest/actions/get-channel-stream-schedule).

## Create Channel Stream Schedule Segment

Creates a stream schedule segment in Twitch.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-channel-stream-schedule-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasterId": "string",
  "startTime": "string",
  "timezone": "string",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-channel-stream-schedule-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasterId": "string",
    "startTime": "string",
    "timezone": "string",
    "duration": 1
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
      "broadcasterId": "string",
      "broadcasterLogin": "string",
      "broadcasterName": "Ava Chen",
      "segments": [
        {
          "canceledUntil": {},
          "category": {},
          "endTime": {},
          "id": "string",
          "isRecurring": true,
          "startTime": "string",
          "title": "string"
        }
      ],
      "vacation": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Channel Stream Schedule Segment action reference](actions/create-channel-stream-schedule-segment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/twitch/latest/actions/create-channel-stream-schedule-segment).
