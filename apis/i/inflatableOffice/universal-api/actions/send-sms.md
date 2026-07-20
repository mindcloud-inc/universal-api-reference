# InflatableOffice: Send SMS

Sends an SMS message from InflatableOffice.

```
POST https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "toNumber": "+15554447777",
  "text": "Hello world"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "toNumber": "+15554447777",
    "text": "Hello world"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `toNumber` | string | yes | Phone number to send the message to. Example: `+15554447777`. |
| `text` | string | yes | Text message content to send. Example: `Hello world`. |
| `fromNumber` | string | no | Optional IO Phone number to send from. Use (999) 999-9999 for test sends. Example: `(999) 999-9999`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "direction": "string",
      "from": "string",
      "id": 1,
      "requestTime": 1,
      "segmentCount": 1,
      "status": 1,
      "text": "string",
      "time": "2026-05-07T12:00:00.000Z",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `direction` | string |  |
| `from` | string |  |
| `id` | number |  |
| `requestTime` | number |  |
| `segmentCount` | number |  |
| `status` | number |  |
| `text` | string |  |
| `time` | date |  |
| `to` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `POST /text` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

