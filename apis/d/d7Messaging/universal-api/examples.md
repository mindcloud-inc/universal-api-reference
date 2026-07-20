# D7 Messaging Universal API Examples

These examples use the MindCloud API key and D7 Messaging connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get SMS Pricing

Retrieves SMS pricing from D7 Messaging.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-sms-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-sms-pricing?${params}`, {
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
      "AE": 1,
      "AU": 1,
      "BR": 1,
      "CA": 1,
      "DE": 1,
      "GB": 1,
      "IN": 1,
      "US": 1
    }
  ],
  "meta": {}
}
```

See the full [Get SMS Pricing action reference](actions/get-sms-pricing.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/d7Messaging/latest/actions/get-sms-pricing).

## Mark WhatsApp Message as Read

Marks a WhatsApp message as read in D7 Messaging.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/mark-whats-app-message-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/mark-whats-app-message-as-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string"
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

See the full [Mark WhatsApp Message as Read action reference](actions/mark-whats-app-message-as-read.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/d7Messaging/latest/actions/mark-whats-app-message-as-read).
