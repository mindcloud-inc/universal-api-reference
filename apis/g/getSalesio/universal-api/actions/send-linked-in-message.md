# GetSales.io: Send LinkedIn Message



```
POST https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/send-linked-in-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/send-linked-in-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/send-linked-in-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderProfileUuid` | string | no | Sender profile UUID. |
| `leadUuid` | string | no | Contact UUID. |
| `templateUuid` | string | no | Template UUID for the message. |
| `text` | string | no | LinkedIn message text. Example: `Hello John, how are you?`. |
| `attachments[]` | array<object> | no | Attachment array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "lead_uuid": "string",
      "sender_profile_uuid": "string",
      "sent_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "team_id": 1,
      "template_uuid": "string",
      "text": "string",
      "user_id": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `lead_uuid` | string |  |
| `sender_profile_uuid` | string |  |
| `sent_at` | date |  |
| `status` | string |  |
| `team_id` | number |  |
| `template_uuid` | string |  |
| `text` | string |  |
| `user_id` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native GetSales.io API, this operation is `POST /flows/api/linkedin-messages` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-linked-in-message.md) for the provider-specific parameters and requirements.

