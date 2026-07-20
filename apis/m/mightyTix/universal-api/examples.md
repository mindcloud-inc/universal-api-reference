# Mighty Tix Universal API Examples

These examples use the MindCloud API key and Mighty Tix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from Mighty Tix.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/get-account?${params}`, {
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
      "currency": "string",
      "locale": "string",
      "name": "Ava Chen",
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mightyTix/latest/actions/get-account).

## Add Session Ticket Types To Session

Adds session ticket types to a session in Mighty Tix.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/add-session-ticket-types-to-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/add-session-ticket-types-to-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input": {}
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
      "end": "2026-05-07T12:00:00.000Z",
      "eventId": "string",
      "id": "string",
      "sessionTicketTypes": [
        {}
      ],
      "start": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Session Ticket Types To Session action reference](actions/add-session-ticket-types-to-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mightyTix/latest/actions/add-session-ticket-types-to-session).
