# Fliqr AI: Send Text Message To Contact

Sends a text message to a contact in Fliqr AI.

```
POST https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/send-text-message-to-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliqr AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/send-text-message-to-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/send-text-message-to-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | Fliqr contact user ID. |
| `text` | string | no | Text message content. |
| `channel` | string | no | Messaging channel. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Fliqr AI API, this operation is `POST /users/:user_id/send/text` (base URL `https://app.fliqr.ai/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-text-message-to-contact.md) for the provider-specific parameters and requirements.

