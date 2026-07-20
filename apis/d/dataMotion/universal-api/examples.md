# DataMotion Universal API Examples

These examples use the MindCloud API key and DataMotion connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Track Secure Message

Retrieves secure message tracking details from DataMotion.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/track-secure-message?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/track-secure-message?${params}`, {
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
      "Attachments": [
        {}
      ],
      "Cost": 1,
      "ExpirationDate": "2026-05-07T12:00:00.000Z",
      "MessageId": 1,
      "MessageSize": 1,
      "SecurityEnvelope": {},
      "Subject": "string",
      "Tracking": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Track Secure Message action reference](actions/track-secure-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataMotion/latest/actions/track-secure-message).

## Send Secure Message

Sends a secure message through DataMotion.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/send-secure-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/send-secure-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string"
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
      "ApplicationId": "string",
      "Expiration": "2026-05-07T12:00:00.000Z",
      "MessageSize": 1,
      "NumberOfRecipients": 1,
      "ProjectId": "string",
      "TransactionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Secure Message action reference](actions/send-secure-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataMotion/latest/actions/send-secure-message).
