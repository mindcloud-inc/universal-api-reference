# BulkSMS: Send Messages

Sends one or more messages through BulkSMS.

```
POST https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/send-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/send-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/send-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | Recipient phone number, recipient list, or group recipient details. |
| `body` | string | yes | SMS message content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no | Optional sender ID or sender object. |
| `encoding` | list | no | Message encoding. Defaults to TEXT when omitted. One of: `0`, `1`, `2`. |
| `routingGroup` | list | no | BulkSMS routing group. One of: `0`, `1`, `2`. |
| `longMessageMaxParts` | number | no | Maximum number of parts for a concatenated message. |
| `userSuppliedId` | string | no | Client correlation value for sent messages, up to 20 characters. |
| `deliveryReports` | list | no | Delivery report mode requested from the delivering network. One of: `0`, `1`, `2`. |
| `autoUnicode` | boolean | no | Automatically convert text to UNICODE when needed. |
| `scheduleDate` | date | no | ISO-8601 date/time when BulkSMS should send the message. |
| `scheduleDescription` | string | no | Description for the scheduled message. |
| `deduplicationId` | number | no | Integer used by BulkSMS to avoid duplicate submissions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "id": "string",
      "status": {},
      "submission": {},
      "to": "string",
      "type": "string",
      "userSuppliedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `id` | string |  |
| `status` | object |  |
| `submission` | object |  |
| `to` | string |  |
| `type` | string |  |
| `userSuppliedId` | string |  |

## Native endpoint

Through the native BulkSMS API, this operation is `POST /messages` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-messages.md) for the provider-specific parameters and requirements.

