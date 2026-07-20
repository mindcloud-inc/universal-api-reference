# NiftyImages Universal API Examples

These examples use the MindCloud API key and NiftyImages connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Widgets

Retrieves widgets from NiftyImages.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-widgets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-widgets?${params}`, {
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
      "Name": "Ava Chen",
      "WidgetKey": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Widgets action reference](actions/list-widgets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/niftyImages/latest/actions/list-widgets).

## Add Map Location

Creates a new map location in NiftyImages.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/add-map-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "Address": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/add-map-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "Address": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Map Location action reference](actions/add-map-location.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/niftyImages/latest/actions/add-map-location).
