# EbulkSMS Universal API Examples

These examples use the MindCloud API key and EbulkSMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Balance

Retrieves your EbulkSMS account balance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/get-account-balance?${params}`, {
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
      "response": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Balance action reference](actions/get-account-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ebulkSMS/latest/actions/get-account-balance).

## Send SMS

Sends an SMS with EbulkSMS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "SMS.message.messagetext": "string",
  "SMS.message.sender": "string",
  "SMS.recipients.gsm[].msidn": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "SMS.message.messagetext": "string",
    "SMS.message.sender": "string",
    "SMS.recipients.gsm[].msidn": "string"
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
      "response": {
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Send SMS action reference](actions/send-sms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ebulkSMS/latest/actions/send-sms).
