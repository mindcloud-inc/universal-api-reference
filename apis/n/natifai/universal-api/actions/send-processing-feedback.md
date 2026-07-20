# Natif.ai: Send Processing Feedback

Creates processing feedback for a document in Natif.ai.

```
POST https://connect.mindcloud.co/v1/universal/natifai/latest/actions/send-processing-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/send-processing-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "processingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/natifai/latest/actions/send-processing-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "processingId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processingId` | string | yes | UUID of the processing request. |
| `description` | string | no | Free-text feedback description for annotation guidance. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tag` | string | no | Optional categorization tag for training data. |
| `expectedClass` | string | no | Expected document class, when known. |
| `expectedSubDocuments[]` | array<object> | no | Expected sub-document split structure for splitting workflows. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Natif.ai API returns.

## Native endpoint

Through the native Natif.ai API, this operation is `POST /processing/feedback/[:processingId]` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-processing-feedback.md) for the provider-specific parameters and requirements.

