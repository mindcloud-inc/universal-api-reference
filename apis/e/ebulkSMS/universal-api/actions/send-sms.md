# EbulkSMS: Send SMS

Sends an SMS with EbulkSMS.

```
POST https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EbulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `SMS` | object | no | Root SMS payload object. |
| `SMS.dndsender` | number | no | Use 1 to enable MTN DND delivery or 0 to disable it. Default: `0`. |
| `SMS.message` | object | no | Message details object. |
| `SMS.message.flash` | number | no | Use 1 for flash SMS or 0 for a normal SMS. Default: `0`. |
| `SMS.message.messagetext` | string | yes | The SMS content to send. |
| `SMS.message.sender` | string | yes | Sender name shown to recipients. |
| `SMS.recipients` | object | no | Recipients wrapper object. |
| `SMS.recipients.gsm[]` | array<object> | no | Recipient records. |
| `SMS.recipients.gsm[].msgid` | string | no | Optional unique ID for delivery-report tracking. |
| `SMS.recipients.gsm[].msidn` | string | yes | Recipient phone number in full international format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EbulkSMS API returns.

## Native endpoint

Through the native EbulkSMS API, this operation is `POST /sendsms.json` (base URL `https://api.ebulksms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

