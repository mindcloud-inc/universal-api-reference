# Channex Universal API Examples

These examples use the MindCloud API key and Channex connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Properties

Retrieves properties from your Channex account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-properties?${params}`, {
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
      "data": [
        {
          "attributes": {
            "city": "string",
            "country": "string",
            "currency": "string",
            "is_active": true,
            "title": "string"
          },
          "id": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Properties action reference](actions/list-properties.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/channex/latest/actions/list-properties).

## Acknowledge Booking Revision

Acknowledges a booking revision in Channex.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channex/latest/actions/acknowledge-booking-revision" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/acknowledge-booking-revision', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "meta": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Acknowledge Booking Revision action reference](actions/acknowledge-booking-revision.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/channex/latest/actions/acknowledge-booking-revision).
