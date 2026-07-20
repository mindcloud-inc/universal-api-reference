# NeetoCal Universal API Examples

These examples use the MindCloud API key and NeetoCal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bookings

Finds bookings in NeetoCal by filter criteria.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/list-bookings?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Bookings action reference](actions/list-bookings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neetoCal/latest/actions/list-bookings).

## Create Duration

Creates a new meeting duration in NeetoCal.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/create-meeting-duration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meeting_sid": "string",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/create-meeting-duration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meeting_sid": "string",
    "duration": 1
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

See the full [Create Duration action reference](actions/create-meeting-duration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neetoCal/latest/actions/create-meeting-duration).
