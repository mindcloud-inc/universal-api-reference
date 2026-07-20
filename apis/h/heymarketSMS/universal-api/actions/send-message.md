# Heymarket SMS: Send Message



```
POST https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": 1,
  "creatorId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": 1,
    "creatorId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | number | yes | Unique identifier for the inbox from which the message will be sent. |
| `creatorId` | number | yes | Unique identifier for the sender. |
| `phoneNumber` | string | no | Target phone number in E.164 format without the plus sign. Example: `15555550123`. |
| `text` | string | no | Message text body. Example: `Hello from MindCloud`. |
| `templateId` | number | no | Unique identifier of the Heymarket template. |
| `localId` | string | no | Client unique identifier for the message. Example: `msg-001`. |
| `private` | boolean | no | Create a private comment within a Heymarket conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compliance_results": {},
      "convo_id": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "queued": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compliance_results` | object |  |
| `convo_id` | number |  |
| `date` | date |  |
| `id` | number |  |
| `queued` | boolean |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `POST /v1/message/send` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

