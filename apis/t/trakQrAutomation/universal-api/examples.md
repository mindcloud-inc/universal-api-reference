# Trak Qr Automation Universal API Examples

These examples use the MindCloud API key and Trak Qr Automation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Partner Balance

Retrieves partner balance from Trak Qr Automation.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/get-partner-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/get-partner-balance?${params}`, {
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
      "attendeesCount": 1,
      "eventId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Partner Balance action reference](actions/get-partner-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trakQrAutomation/latest/actions/get-partner-balance).

## Create Attendee

Creates a new attendee for an event in Trak Qr Automation.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-attendee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventKey": "string",
  "attachments[]": [
    {}
  ],
  "attachments[].kind": "string",
  "attachments[].val": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-attendee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventKey": "string",
    "attachments[]": [{}],
    "attachments[].kind": "string",
    "attachments[].val": "string"
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
      "pdfUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Attendee action reference](actions/create-attendee.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trakQrAutomation/latest/actions/create-attendee).
