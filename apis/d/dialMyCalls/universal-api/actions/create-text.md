# DialMyCalls: Create Text

Creates a new text in DialMyCalls.

```
POST https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/create-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DialMyCalls `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/create-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ],
  "contacts[].phone": "string",
  "keywordId": "string",
  "messages[]": [
    "string"
  ],
  "name": "Ava Chen",
  "vanitynumberId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/create-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}],
    "contacts[].phone": "string",
    "keywordId": "string",
    "messages[]": ["string"],
    "name": "Ava Chen",
    "vanitynumberId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessaccountId` | string | no | Schedule this broadcast as an access account. |
| `concatenateSms` | boolean | no | Combine all SMS messages into one message on the end user's device. |
| `contacts[]` | array<object> | yes | List of contact information that should receive the broadcast. |
| `contacts[].email` | string | no | Contact email address. |
| `contacts[].firstname` | string | no | Contact first name. |
| `contacts[].lastname` | string | no | Contact last name. |
| `contacts[].phone` | string | yes | Contact phone number. |
| `keywordId` | string | yes | The keyword ID that should be associated with this broadcast. |
| `messages[]` | array<string> | yes | List of messages to send, up to 10. |
| `name` | string | yes | Name the broadcast. |
| `sendAt` | string | no | When the broadcast should be sent in UTC timestamp format like 2026-03-27T23:00:00+0000. |
| `sendEmail` | boolean | no | Also send an email to the contacts. |
| `sendImmediately` | boolean | no | Whether the broadcast should go out immediately. |
| `shortcodeId` | string | no | The shortcode ID that the broadcast will be sent from. |
| `vanitynumberId` | string | yes | The vanity number that the text broadcast will be sent from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessaccountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditCost": 1,
      "id": "string",
      "name": "Ava Chen",
      "pendingCancel": true,
      "sendAt": "string",
      "totalRecipients": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessaccountId` | string | Access account ID when applicable. |
| `createdAt` | date | When the broadcast was created. |
| `creditCost` | number | Credits used by the broadcast. |
| `id` | string | Broadcast ID. |
| `name` | string | Broadcast name. |
| `pendingCancel` | boolean | Whether cancelation is pending. |
| `sendAt` | string | Scheduled UTC send timestamp. |
| `totalRecipients` | number | Recipient count. |
| `updatedAt` | date | When the broadcast was updated. |

## Native endpoint

Through the native DialMyCalls API, this operation is `POST /service/text` (base URL `https://{{credentials.apiKey}}@api.dialmycalls.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text.md) for the provider-specific parameters and requirements.

