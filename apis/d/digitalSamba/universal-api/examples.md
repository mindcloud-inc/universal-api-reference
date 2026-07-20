# Digital Samba Universal API Examples

These examples use the MindCloud API key and Digital Samba connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get all team rooms

Retrieves team rooms from Digital Samba.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-team-rooms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-team-rooms?${params}`, {
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
      "audioOnJoinEnabled": true,
      "audioQuality": "string",
      "autoPipEnabled": true,
      "backgroundColor": "string",
      "description": "string",
      "friendlyUrl": "https://example.com",
      "hdVideoQuality": "string",
      "id": "string",
      "language": "string",
      "languages": [
        "string"
      ],
      "languageSelectionEnabled": true,
      "maxBroadcasters": 1,
      "maxParticipants": 1,
      "paletteMode": "string",
      "pipEnabled": true,
      "primaryColor": "string",
      "privacy": "string",
      "roomReactionsEnabled": true,
      "toolbarColor": "string",
      "toolbarEnabled": true,
      "toolbarPosition": "string",
      "topbarEnabled": true,
      "topic": "string",
      "videoOnJoinEnabled": true
    }
  ],
  "meta": {}
}
```

See the full [Get all team rooms action reference](actions/get-all-team-rooms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digitalSamba/latest/actions/get-all-team-rooms).

## Archive recording

Updates a recording to archived in Digital Samba.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/archive-recording" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recording": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/archive-recording', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recording": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Archive recording action reference](actions/archive-recording.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digitalSamba/latest/actions/archive-recording).
