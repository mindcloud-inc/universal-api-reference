# CRM Messaging Universal API Examples

These examples use the MindCloud API key and CRM Messaging connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Messages

Retrieves messages from CRM Messaging.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/list-messages?${params}`, {
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
      "channel": "string",
      "creditsConsumed": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "deliveryStatus": "string",
      "direction": "string",
      "errorCode": "string",
      "from": "string",
      "id": 1,
      "message": "string",
      "msgId": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Messages action reference](actions/list-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cRMMessaging/latest/actions/list-messages).

## Create Contact

Creates a new contact in CRM Messaging.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cRMMessaging/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "string"
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
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cRMMessaging/latest/actions/create-contact).
