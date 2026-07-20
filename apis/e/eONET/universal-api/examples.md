# EONET Universal API Examples

These examples use the MindCloud API key and EONET connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events

Retrieves events from EONET.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eONET/latest/actions/list-events?${params}`, {
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
      "categories": [
        {
          "id": "string",
          "title": "string"
        }
      ],
      "closed": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "geometry": [
        {
          "coordinates": [
            1
          ],
          "date": "2026-05-07T12:00:00.000Z",
          "magnitudeUnit": "string",
          "magnitudeValue": 1,
          "type": "string"
        }
      ],
      "id": "string",
      "link": "https://example.com",
      "sources": [
        {
          "id": "string",
          "url": "https://example.com"
        }
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eONET/latest/actions/list-events).
