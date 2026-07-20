# Sempico Solutions SMS: Send Bulk SMS



```
POST https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/send-bulk-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/send-bulk-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "senderID": "string",
  "text": "string",
  "id_group[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/send-bulk-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "senderID": "string",
    "text": "string",
    "id_group[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderID` | string | yes | Sender ID for the bulk message. |
| `text` | string | yes | Bulk SMS message text. |
| `id_group[]` | array<number> | yes | Group IDs to send the bulk SMS to. |
| `phone[]` | array<string> | no | Optional extra phone numbers to include. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id_group_excluded[]` | array<number> | no | Optional group IDs to exclude from the sending. |
| `dateStart` | date | no | Optional date to start gradual sending. |
| `timeStart` | string | no | Optional start time for gradual sending. |
| `timeStop` | string | no | Optional stop time for gradual sending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {
        "id_group": [
          1
        ],
        "senderID": "string",
        "sentID": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details.id_group` | array<number> | Group IDs used for sending. |
| `details.senderID` | string | Sender ID used for the send. |
| `details.sentID` | number | Sempico sent batch ID. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /send-bulk` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-bulk-sms.md) for the provider-specific parameters and requirements.

