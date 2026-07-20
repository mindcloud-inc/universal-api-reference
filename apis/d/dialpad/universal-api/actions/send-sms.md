# Dialpad: Send SMS

Sends an SMS message from Dialpad.

```
POST https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/send-sms', {
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
| `text` | string | no | The contents of the message that should be sent. |
| `to_numbers[]` | array<string> | no | Up to 10 E164-formatted phone numbers who should receive the SMS. |
| `user_id` | number | no | The ID of the user who should be the sender of the SMS. |
| `from_number` | string | no | The sender number. This overrides user_id and sender_group_id. |
| `sender_group_id` | number | no | The ID of an office, department, or call center that the user should send the message on behalf of. |
| `sender_group_type` | string | no | The sender group's type. |
| `channel_hashtag` | string | no | The hashtag of the channel which should receive the SMS. |
| `infer_country_code` | boolean | no | If true, to_numbers will be assumed to be from the specified user's country. Default: `false`. |
| `media` | string | no | Base64-encoded media attachment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "createdDate": "string",
      "deviceType": "string",
      "direction": "string",
      "fromNumber": "string",
      "id": "string",
      "messageStatus": "string",
      "targetId": "string",
      "targetType": "string",
      "text": "string",
      "toNumbers": [
        "string"
      ],
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `createdDate` | string |  |
| `deviceType` | string |  |
| `direction` | string |  |
| `fromNumber` | string |  |
| `id` | string |  |
| `messageStatus` | string |  |
| `targetId` | string |  |
| `targetType` | string |  |
| `text` | string |  |
| `toNumbers[]` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Dialpad API, this operation is `POST /sms` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

