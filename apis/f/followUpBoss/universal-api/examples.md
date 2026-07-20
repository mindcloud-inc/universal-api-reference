# Follow Up Boss - Legacy Universal API Examples

These examples use the MindCloud API key and Follow Up Boss - Legacy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events

Retrieves events from Follow Up Boss - Legacy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBoss/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBoss/latest/actions/list-events?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "message": "string",
      "occurred": "2026-05-07T12:00:00.000Z",
      "pageDuration": 1,
      "pageUrl": "https://example.com",
      "personId": 1,
      "property": {
        "city": "string",
        "code": "string",
        "forRent": 1,
        "id": 1,
        "lat": 1,
        "lng": 1,
        "lot": "string",
        "mlsNumber": "string",
        "price": "string",
        "state": "string",
        "street": "string",
        "type": "string",
        "url": "https://example.com"
      },
      "source": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/followUpBoss/latest/actions/list-events).
