# Extracta.ai: Get Classification Batch Results

Retrieves classification batch results from Extracta.ai.

```
GET https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/get-classification-batch-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/get-classification-batch-results?connectionId=$CONNECTION_ID&classificationId=string&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "classificationId": "string",
  "batchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/get-classification-batch-results?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classificationId` | string | yes | Unique identifier for the classification. |
| `batchId` | string | yes | Unique identifier for the batch. |

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

Through the native Extracta.ai API, this operation is `POST /documentClassification/getResults` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-classification-batch-results.md) for the provider-specific parameters and requirements.

