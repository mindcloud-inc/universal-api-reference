# JustCall: Send SMS/MMS

Creates an SMS or MMS message in JustCall.

```
POST https://connect.mindcloud.co/v1/universal/justCall/latest/actions/send-sms-mms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/send-sms-mms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "justcallNumber": "string",
  "body": "string",
  "contactNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/justCall/latest/actions/send-sms-mms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "justcallNumber": "string",
    "body": "string",
    "contactNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `justcallNumber` | string | yes |  |
| `body` | string | yes |  |
| `contactNumber` | string | yes |  |
| `mediaUrl` | string | no |  |
| `restrictOnce` | string | no |  |
| `scheduleAt` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentEmail": "ava@example.com",
      "agentId": 1,
      "agentName": "Ava Chen",
      "contactEmail": "ava@example.com",
      "contactName": "Ava Chen",
      "contactNumber": "string",
      "costIncurred": 1,
      "deliveryStatus": "string",
      "direction": "string",
      "id": 1,
      "isDeleted": true,
      "justcallLineName": "Ava Chen",
      "justcallNumber": "string",
      "medium": "string",
      "smsDate": "string",
      "smsInfo": {},
      "smsTime": "string",
      "smsUserDate": "string",
      "smsUserTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentEmail` | string |  |
| `agentId` | number |  |
| `agentName` | string |  |
| `contactEmail` | string |  |
| `contactName` | string |  |
| `contactNumber` | string |  |
| `costIncurred` | number |  |
| `deliveryStatus` | string |  |
| `direction` | string |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `justcallLineName` | string |  |
| `justcallNumber` | string |  |
| `medium` | string |  |
| `smsDate` | string |  |
| `smsInfo` | object |  |
| `smsTime` | string |  |
| `smsUserDate` | string |  |
| `smsUserTime` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `POST /v2.1/texts/new` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-mms.md) for the provider-specific parameters and requirements.

