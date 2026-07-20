# httpSMS Universal API Examples

These examples use the MindCloud API key and httpSMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Messages



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/httpSMS/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&contact=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "owner": "string",
  "contact": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/httpSMS/latest/actions/list-messages?${params}`, {
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
      "attachments": [
        "string"
      ],
      "contact": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deliveredAt": "2026-05-07T12:00:00.000Z",
      "encrypted": true,
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "failedAt": "2026-05-07T12:00:00.000Z",
      "failureReason": "string",
      "id": "string",
      "lastAttemptedAt": "2026-05-07T12:00:00.000Z",
      "maxSendAttempts": 1,
      "orderTimestamp": "2026-05-07T12:00:00.000Z",
      "owner": "string",
      "receivedAt": "2026-05-07T12:00:00.000Z",
      "requestId": "string",
      "requestReceivedAt": "2026-05-07T12:00:00.000Z",
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "scheduledSendTime": "2026-05-07T12:00:00.000Z",
      "sendAttemptCount": 1,
      "sendTime": 1,
      "sentAt": "2026-05-07T12:00:00.000Z",
      "sim": "string",
      "status": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Messages action reference](actions/list-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/httpSMS/latest/actions/list-messages).
