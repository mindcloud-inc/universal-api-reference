# ClickMeeting Universal API Examples

These examples use the MindCloud API key and ClickMeeting connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Phone Gateways

Retrieves available phone gateways from ClickMeeting.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-phone-gateways?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-phone-gateways?${params}`, {
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
      "code": "string",
      "geo": {
        "lat": 1,
        "long": 1
      },
      "location": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Phone Gateways action reference](actions/list-phone-gateways.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clickMeeting/latest/actions/list-phone-gateways).

## Create Conference

Creates a new conference in ClickMeeting.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/create-conference" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "room_type": "meeting",
  "permanent_room": true,
  "access_type": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/create-conference', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "room_type": "meeting",
    "permanent_room": true,
    "access_type": "1"
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
      "room": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "embed_room_url": "https://example.com",
        "id": 1,
        "name": "Ava Chen",
        "permanent_room": true,
        "room_type": "string",
        "room_url": "https://example.com",
        "starts_at": "2026-05-07T12:00:00.000Z",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Conference action reference](actions/create-conference.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clickMeeting/latest/actions/create-conference).
