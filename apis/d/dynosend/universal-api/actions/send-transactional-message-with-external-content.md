# Dynosend: Send Transactional Message with External Content

Creates a transactional message in Dynosend with external content.

```
POST https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/send-transactional-message-with-external-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/send-transactional-message-with-external-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "htmlBody": "string",
  "recipient": "string",
  "textBody": "string",
  "transactionalUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/send-transactional-message-with-external-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "htmlBody": "string",
    "recipient": "string",
    "textBody": "string",
    "transactionalUid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `htmlBody` | string | yes | The HTML content to send when the transactional template uses external content. |
| `recipient` | string | yes | The email address that should receive the transactional message. |
| `textBody` | string | yes | The plain-text content to send when the transactional template uses external content. |
| `transactionalUid` | string | yes | The UID of the Dynosend transactional message to send. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dynosend API returns.

## Native endpoint

Through the native Dynosend API, this operation is `POST /transactional` (base URL `https://api.dynosend.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-message-with-external-content.md) for the provider-specific parameters and requirements.

