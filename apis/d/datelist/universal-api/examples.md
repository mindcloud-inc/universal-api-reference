# Datelist Universal API Examples

These examples use the MindCloud API key and Datelist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Calendars

Retrieves available calendars from your Datelist account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-calendars?${params}`, {
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Calendars action reference](actions/list-calendars.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datelist/latest/actions/list-calendars).

## Create Webhook

Creates a new webhook in Datelist for booking notifications.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datelist/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "calendarId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datelist/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "calendarId": 1
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
      "calendarId": 1,
      "createdAt": "string",
      "id": 1,
      "updatedAt": "string",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datelist/latest/actions/create-webhook).
