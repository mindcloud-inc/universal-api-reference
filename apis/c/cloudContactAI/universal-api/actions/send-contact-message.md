# CloudContactAI: Send Contact Message



```
POST https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/send-contact-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/send-contact-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/send-contact-message', {
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
| `contactId` | string | no | The contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "contactFirstName": "Ava",
      "contactLastName": "Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isArchived": true,
      "message": "string",
      "phone": "string",
      "segments": 1,
      "sentAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "twilioErrorCode": "string",
      "twilioErrorMessage": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userClientId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `contactFirstName` | string |  |
| `contactLastName` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `message` | string |  |
| `phone` | string |  |
| `segments` | number |  |
| `sentAt` | date |  |
| `status` | string |  |
| `twilioErrorCode` | string |  |
| `twilioErrorMessage` | string |  |
| `updatedAt` | date |  |
| `userClientId` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `POST api/v2/messages/contact/:contactId/send` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-contact-message.md) for the provider-specific parameters and requirements.

