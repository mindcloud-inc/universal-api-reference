# Range: Record Activity

Record an activity interaction for a user with attachment data.

```
POST https://connect.mindcloud.co/v1/universal/range/latest/actions/record-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/range/latest/actions/record-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/range/latest/actions/record-activity', {
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
| `attachment` | object | no | Attachment object to upsert with the interaction. |
| `attachmentId` | string | no | Existing attachment ID to associate with the interaction. |
| `idempotencyKey` | string | no | Optional de-duplication key. |
| `interactionAt` | string | no | Timestamp when the interaction occurred. |
| `interactionType` | number | no | The interaction type enum value. |
| `userId` | string | no | The user who should receive the activity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentId": "string",
      "interactionId": "string",
      "success": true,
      "wasRecorded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentId` | string |  |
| `interactionId` | string |  |
| `success` | boolean |  |
| `wasRecorded` | boolean |  |

## Native endpoint

Through the native Range API, this operation is `POST /v1/activity` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-activity.md) for the provider-specific parameters and requirements.

