# Sequenzy: Create Sequence with AI

Creates an AI-generated sequence in Sequenzy.

```
POST https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/create-sequence-with-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/create-sequence-with-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventName": "Ava Chen",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/create-sequence-with-ai', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventName": "Ava Chen",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventName` | string | yes | Trigger event name. |
| `goal` | string | no | What the sequence should accomplish. |
| `name` | string | yes | Sequence name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventTrackingCode": "string",
      "message": "string",
      "requiredEvents": [
        "string"
      ],
      "sequence": {
        "emailCount": 1,
        "enrichmentStatus": "string",
        "id": "string",
        "name": "Ava Chen",
        "status": "string",
        "trigger": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventTrackingCode` | string |  |
| `message` | string |  |
| `requiredEvents` | array<string> |  |
| `sequence.emailCount` | number |  |
| `sequence.enrichmentStatus` | string |  |
| `sequence.id` | string |  |
| `sequence.name` | string |  |
| `sequence.status` | string |  |
| `sequence.trigger` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `POST /sequences` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sequence-with-ai.md) for the provider-specific parameters and requirements.

