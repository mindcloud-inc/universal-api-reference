# tl:dv Universal API Examples

These examples use the MindCloud API key and tl:dv connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Meetings

Retrieves meetings from tl:dv.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tldv/latest/actions/list-meetings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tldv/latest/actions/list-meetings?${params}`, {
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
      "duration": 1,
      "extraProperties": {},
      "happenedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invitees": [
        {}
      ],
      "name": "Ava Chen",
      "organizer": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Meetings action reference](actions/list-meetings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tldv/latest/actions/list-meetings).

## Import Meeting

Imports a meeting into tl:dv from a URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tldv/latest/actions/import-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tldv/latest/actions/import-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com"
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
      "jobId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Import Meeting action reference](actions/import-meeting.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tldv/latest/actions/import-meeting).
