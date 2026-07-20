# Extracta.ai: Get Extraction File Results

Retrieves extraction file results from Extracta.ai.

```
GET https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/get-extraction-file-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/get-extraction-file-results?connectionId=$CONNECTION_ID&extractionId=string&batchId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extractionId": "string",
  "batchId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/get-extraction-file-results?${params}`, {
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
| `extractionId` | string | yes | Unique identifier for the extraction. |
| `batchId` | string | yes | Unique identifier for the batch. |
| `fileId` | string | yes | Unique identifier for the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "extractionId": "string",
      "fileId": "string",
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
| `extractionId` | string |  |
| `fileId` | string |  |
| `files` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Extracta.ai API, this operation is `POST /getBatchResults` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extraction-file-results.md) for the provider-specific parameters and requirements.

