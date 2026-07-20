# LiveKit Universal API Examples

These examples use the MindCloud API key and LiveKit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Rooms

Retrieves rooms from LiveKit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/list-rooms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/list-rooms?${params}`, {
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
      "rooms": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Rooms action reference](actions/list-rooms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/liveKit/latest/actions/list-rooms).

## Create Ingress

Creates a new ingress in LiveKit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/create-ingress" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputType": "string",
  "roomName": "Ava Chen",
  "participantIdentity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/create-ingress', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputType": "string",
    "roomName": "Ava Chen",
    "participantIdentity": "string"
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
      "audio": {},
      "bypass_transcoding": true,
      "enable_transcoding": true,
      "ingress_id": "string",
      "input_type": "string",
      "name": "Ava Chen",
      "participant_identity": "string",
      "participant_metadata": "string",
      "participant_name": "Ava Chen",
      "reusable": true,
      "room_name": "Ava Chen",
      "state": {},
      "stream_key": "string",
      "url": "https://example.com",
      "video": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Ingress action reference](actions/create-ingress.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/liveKit/latest/actions/create-ingress).
