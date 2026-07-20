# Messaggio Universal API Examples

These examples use the MindCloud API key and Messaggio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Credentials

Validates stored Messaggio credentials against the bulk API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/validate-credentials?${params}`, {
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
      "code": "string",
      "techMessage": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Credentials action reference](actions/validate-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/messaggio/latest/actions/validate-credentials).

## Send Flash Call Code

Creates a flash call code in Messaggio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-flash-call-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipientPhone": "15551234567",
  "senderCode": "FLASHID",
  "verificationCode": "1234"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-flash-call-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipientPhone": "15551234567",
    "senderCode": "FLASHID",
    "verificationCode": "1234"
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
      "accepted_at": "string",
      "messages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Send Flash Call Code action reference](actions/send-flash-call-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/messaggio/latest/actions/send-flash-call-code).
