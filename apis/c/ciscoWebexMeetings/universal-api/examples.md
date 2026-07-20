# Cisco Webex Meetings Universal API Examples

These examples use the MindCloud API key and Cisco Webex Meetings connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Meetings

Retrieves meetings from Cisco Webex Meetings.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/list-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/list-meetings?${params}`, {
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
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Meetings action reference](actions/list-meetings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ciscoWebexMeetings/latest/actions/list-meetings).

## Create a Meeting

Creates a new meeting in Cisco Webex Meetings.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/create-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ciscoWebexMeetings/latest/actions/create-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "agenda": "string",
      "enabledBreakoutSessions": true,
      "end": "string",
      "hostDisplayName": "Ava Chen",
      "hostEmail": "ava@example.com",
      "hostUserId": "string",
      "id": "string",
      "meetingNumber": "string",
      "meetingType": "string",
      "siteUrl": "https://example.com",
      "start": "string",
      "state": "string",
      "telephony": {},
      "timezone": "string",
      "title": "string",
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create a Meeting action reference](actions/create-meeting.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ciscoWebexMeetings/latest/actions/create-meeting).
