# LLMWhisperer: Get Extraction Details

Retrieves details for an LLMWhisperer extraction job.

```
GET https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-extraction-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMWhisperer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-extraction-details?connectionId=$CONNECTION_ID&whisperHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "whisperHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-extraction-details?${params}`, {
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
| `whisperHash` | string | yes | Extraction job hash returned by the extraction API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_at": "string",
      "mode": "string",
      "processed_pages": 1,
      "processing_started_at": "string",
      "processing_time_in_seconds": 1,
      "requested_pages": 1,
      "tag": "string",
      "total_pages": 1,
      "upload_file_size_in_kb": 1,
      "whisper_hash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_at` | string |  |
| `mode` | string |  |
| `processed_pages` | number |  |
| `processing_started_at` | string |  |
| `processing_time_in_seconds` | number |  |
| `requested_pages` | number |  |
| `tag` | string |  |
| `total_pages` | number |  |
| `upload_file_size_in_kb` | number |  |
| `whisper_hash` | string |  |

## Native endpoint

Through the native LLMWhisperer API, this operation is `GET /whisper-detail` (base URL `https://llmwhisperer-api.us-central.unstract.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extraction-details.md) for the provider-specific parameters and requirements.

