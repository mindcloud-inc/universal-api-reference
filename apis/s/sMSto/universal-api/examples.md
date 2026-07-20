# SMS.to Universal API Examples

These examples use the MindCloud API key and SMS.to connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Last Message

Retrieves the most recent sent message from SMS.to.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-last-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-last-message?${params}`, {
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
      "callbackUrl": "https://example.com",
      "campaignId": "string",
      "cost": 1,
      "createdAt": "string",
      "failedReason": "string",
      "id": "string",
      "internalFailedReason": "string",
      "isApi": true,
      "message": "string",
      "scheduledFor": "string",
      "senderId": "string",
      "sentAt": "string",
      "smsCount": 1,
      "status": "string",
      "timezone": "string",
      "to": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Last Message action reference](actions/get-last-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSto/latest/actions/get-last-message).

## Schedule Sending Messages

Schedules personalized SMS messages for later delivery in SMS.to.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/schedule-sending-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ],
  "messages[].message": "string",
  "messages[].to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/schedule-sending-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}],
    "messages[].message": "string",
    "messages[].to": "string"
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
      "campaignId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Schedule Sending Messages action reference](actions/schedule-sending-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSto/latest/actions/schedule-sending-messages).
