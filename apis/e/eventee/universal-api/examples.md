# Eventee Universal API Examples

These examples use the MindCloud API key and Eventee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Event Content

Retrieves event content from Eventee.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/get-event-content?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventee/latest/actions/get-event-content?${params}`, {
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
      "days": [
        {}
      ],
      "halls": [
        {}
      ],
      "lectures": [
        {}
      ],
      "pauses": [
        {}
      ],
      "speakers": [
        {}
      ],
      "tracks": [
        {}
      ],
      "workshops": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Event Content action reference](actions/get-event-content.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventee/latest/actions/get-event-content).

## Create Hall

Creates a hall in Eventee.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-hall" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-hall', {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Hall action reference](actions/create-hall.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventee/latest/actions/create-hall).
