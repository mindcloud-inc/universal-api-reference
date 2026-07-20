# EZ Texting: Create Message

Creates a message in EZ Texting.

```
POST https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-message', {
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
| `companyName` | string | no | Company name for the message |
| `fromNumber` | string | no | EZ Texting sender number Example: `(737) 337-8315`. |
| `groupIds[]` | array<string> | no | Recipient contact group IDs |
| `mediaFileId` | string | no | Existing media file ID |
| `mediaUrl` | string | no | Public media URL |
| `message` | string | no | Message text |
| `messageTemplateId` | string | no | Message template ID |
| `messageType` | string | no | Requested message type to send. Allowed values: SMS or MMS. Example: `SMS`. |
| `sendAt` | string | no | Scheduled send time |
| `strictValidation` | boolean | no | Require strict recipient validation |
| `toNumbers[]` | array<string> | no | Recipient phone numbers Example: `(737) 337-8315`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EZ Texting API returns.

## Native endpoint

Through the native EZ Texting API, this operation is `POST /messages` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

