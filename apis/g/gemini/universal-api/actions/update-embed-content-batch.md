# Gemini: Update Embed Content Batch

Updates an embed content batch in Gemini.

```
PUT https://connect.mindcloud.co/v1/universal/gemini/latest/actions/update-embed-content-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/update-embed-content-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gemini/latest/actions/update-embed-content-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Batch operation token without `batches/` prefix, for example `1234567890:updateEmbedContentBatch`. |
| `model` | string | no | Model used by the batch. |
| `displayName` | string | no | Human-readable name for the batch. |
| `inputConfig` | object | no | Batch input configuration object. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateMask` | string | no | Comma-separated field mask for fields to update. |
| `priority` | string | no | Optional batch scheduling priority. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchStats": {},
      "createTime": "string",
      "displayName": "Ava Chen",
      "endTime": "string",
      "inputConfig": {},
      "model": "string",
      "name": "Ava Chen",
      "output": {},
      "priority": "string",
      "state": "string",
      "updateTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchStats` | object | Batch-level processing counters. |
| `createTime` | string | Batch creation timestamp. |
| `displayName` | string | Human-readable batch name. |
| `endTime` | string | Batch completion timestamp. |
| `inputConfig` | object | Input configuration for the batch. |
| `model` | string | Model used by the batch. |
| `name` | string | Batch resource name. |
| `output` | object | Batch output payload. |
| `priority` | string | Batch scheduling priority. |
| `state` | string | Current batch state. |
| `updateTime` | string | Batch update timestamp. |

## Native endpoint

Through the native Gemini API, this operation is `PATCH v1beta/batches/:name` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-embed-content-batch.md) for the provider-specific parameters and requirements.

