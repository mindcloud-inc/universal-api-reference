# Harvestr.io: Create Feedback



```
POST https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/create-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "discoveryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "discoveryId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The message ID to link the feedback to |
| `discoveryId` | string | yes | The discovery ID to link the feedback to |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `score` | number | no | The feedback score (minimum 0) |
| `processMessage` | boolean | no | Mark the message as processed after creating the feedback |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "discoveryId": "string",
      "id": "string",
      "messageId": "string",
      "score": 1,
      "selections": {
        "clientId": "string",
        "content": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "fullSelection": true,
        "id": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "starred": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string | Client identifier |
| `createdAt` | date | Creation date of the feedback |
| `discoveryId` | string | Identifier of the associated discovery |
| `id` | string | Unique identifier of the feedback |
| `messageId` | string | Identifier of the associated message |
| `score` | number | Score associated with the feedback |
| `selections` | array<object> | List of selections within the feedback |
| `selections.clientId` | string | Client identifier |
| `selections.content` | string | Text content of the selection |
| `selections.createdAt` | date | Creation date of the selection |
| `selections.fullSelection` | boolean | Whether this selection covers the full feedback content |
| `selections.id` | string | Unique identifier of the selection |
| `selections.updatedAt` | date | Last update date of the selection |
| `starred` | boolean | Whether the feedback is starred |
| `updatedAt` | date | Last update date of the feedback |

## Native endpoint

Through the native Harvestr.io API, this operation is `POST /feedback` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feedback.md) for the provider-specific parameters and requirements.

