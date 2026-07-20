# ChatBotKit: Ensure Contact Existence



```
POST https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/ensure-contact-existence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/ensure-contact-existence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fingerprint": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/ensure-contact-existence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fingerprint": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name of the contact |
| `description` | string | no | Description of the contact |
| `meta` | object | no | Metadata for the contact |
| `fingerprint` | string | yes | Fingerprint for the contact |
| `email` | string | no | Email address of the contact |
| `phone` | string | no | Phone number of the contact |
| `nick` | string | no | Nickname of the contact |
| `preferences` | string | no | Preferences of the contact |
| `verifiedAt` | number | no | Verification timestamp for the contact |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /contact/ensure` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ensure-contact-existence.md) for the provider-specific parameters and requirements.

