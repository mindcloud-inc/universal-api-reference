# AvoSMS: Send SMS

Sends an SMS with AvoSMS.

```
POST https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipients": "33612345678",
  "message": "MindCloud stage 3 test"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipients": "33612345678",
    "message": "MindCloud stage 3 test"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipients` | string | yes | Recipient phone numbers Example: `33612345678`. |
| `message` | string | yes | SMS content up to 600 characters Example: `MindCloud stage 3 test`. |
| `sender` | string | no | Sender name between 3 and 11 characters Example: `MCLD31A`. |
| `deliveryDate` | string | no | Desired sending date in DD/MM/YYYY format Example: `31/03/2026`. |
| `deliveryHour` | string | no | Desired sending time Example: `14:30`. |
| `type` | string | no | SMS type: N for notification or M for marketing Example: `N`. |
| `clickFollow` | string | no | 0 to disable click tracking, 1 to enable Example: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/sms/send` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

