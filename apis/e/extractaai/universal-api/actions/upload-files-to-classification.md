# Extracta.ai: Upload Files to Classification

Uploads files to a classification in Extracta.ai.

```
POST https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/upload-files-to-classification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/upload-files-to-classification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "classificationId": "string",
  "files": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/upload-files-to-classification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "classificationId": "string",
    "files": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classificationId` | string | yes | Unique identifier for the classification. |
| `files` | file | yes | One or more files to upload. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "classificationId": "string",
      "files": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string |  |
| `classificationId` | string |  |
| `files` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Extracta.ai API, this operation is `POST /documentClassification/uploadFiles` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-files-to-classification.md) for the provider-specific parameters and requirements.

