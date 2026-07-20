# Eventbrite Universal API Examples

These examples use the MindCloud API key and Eventbrite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List My Organizations

Retrieves your organizations from Eventbrite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-my-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-my-organizations?${params}`, {
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
      "created": "string",
      "id": "string",
      "imageId": {},
      "locale": {},
      "name": "Ava Chen",
      "parentId": {},
      "type": "string",
      "vertical": "string"
    }
  ],
  "meta": {}
}
```

See the full [List My Organizations action reference](actions/list-my-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventbrite/latest/actions/list-my-organizations).

## Copy Event

Copies an event in Eventbrite.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/copy-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/copy-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string"
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
      "capacity": 1,
      "capacityIsCustom": true,
      "categoryId": {},
      "changed": "string",
      "created": "string",
      "currency": "string",
      "description": {
        "html": "string",
        "text": "string"
      },
      "end": {
        "local": "string",
        "timezone": "string",
        "utc": "string"
      },
      "facebookEventId": {},
      "formatId": {},
      "hideEndDate": true,
      "hideStartDate": true,
      "id": "string",
      "inventoryType": "string",
      "inviteOnly": true,
      "isExternallyTicketed": true,
      "isFree": true,
      "isLocked": true,
      "isReservedSeating": true,
      "isSeries": true,
      "isSeriesParent": true,
      "listed": true,
      "locale": "string",
      "logo": {},
      "logoId": {},
      "name": {
        "html": "Ava Chen",
        "text": "Ava Chen"
      },
      "onlineEvent": true,
      "organizationId": "string",
      "organizerId": "string",
      "privacySetting": "string",
      "resourceUri": "string",
      "shareable": true,
      "showColorsInSeatmapThumbnail": true,
      "showPickASeat": true,
      "showRemaining": true,
      "showSeatmapThumbnail": true,
      "source": "string",
      "start": {
        "local": "string",
        "timezone": "string",
        "utc": "string"
      },
      "status": "string",
      "subcategoryId": {},
      "summary": "string",
      "txTimeLimit": 1,
      "url": "https://example.com",
      "venueId": {},
      "version": {}
    }
  ],
  "meta": {}
}
```

See the full [Copy Event action reference](actions/copy-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventbrite/latest/actions/copy-event).
