# ECAL Universal API Examples

These examples use the MindCloud API key and ECAL connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Calendars

Retrieves calendars from ECAL.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-calendars?${params}`, {
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
      "categoryIds": [
        "string"
      ],
      "feed": "string",
      "genre": "string",
      "id": "string",
      "latestVersion": 1,
      "name": "Ava Chen",
      "note": "string",
      "publisherId": 1,
      "publisherOrgId": 1,
      "reference": "string",
      "subGenre": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Calendars action reference](actions/list-calendars.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eCAL/latest/actions/list-calendars).

## Add Subscriber Subscriptions

Adds calendar subscriptions to an ECAL subscriber.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/add-subscriber-subscriptions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ecalId": "string",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/add-subscriber-subscriptions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ecalId": "string",
    "requestBody": {}
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
      "calendarIds": [
        "string"
      ],
      "ecalId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Subscriber Subscriptions action reference](actions/add-subscriber-subscriptions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eCAL/latest/actions/add-subscriber-subscriptions).
