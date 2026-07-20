# Schedule It Universal API Examples

These examples use the MindCloud API key and Schedule It connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Groups

Retrieves groups from Schedule It.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/list-groups?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Groups action reference](actions/list-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scheduleIt/latest/actions/list-groups).

## Create Event

Creates a new event in Schedule It.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "owner": 1,
  "dateStart": "string",
  "dateEnd": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "owner": 1,
    "dateStart": "string",
    "dateEnd": "string"
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
      "color_back": "string",
      "color_text": "string",
      "completed": "string",
      "date_end": "string",
      "date_start": "string",
      "geonav": "string",
      "id": "string",
      "location": "string",
      "locked": "string",
      "notes": "string",
      "owner": "string",
      "owner_names_simple": "Ava Chen",
      "parentid": "string",
      "priority": "string",
      "private": "string",
      "starticon": "string",
      "style": "string",
      "title": "string",
      "workingduration": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Event action reference](actions/create-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scheduleIt/latest/actions/create-event).
