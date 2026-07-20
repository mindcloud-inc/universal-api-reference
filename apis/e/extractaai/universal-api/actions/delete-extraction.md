# Extracta.ai: Delete Extraction

Deletes an existing extraction from Extracta.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/delete-extraction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/delete-extraction?connectionId=$CONNECTION_ID&extractionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extractionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/delete-extraction?${params}`, {
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
| `batchId` | string | no | Unique identifier for the batch. |
| `fileId` | string | no | Unique identifier for the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedAt": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedAt` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Extracta.ai API, this operation is `DELETE /deleteExtraction` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-extraction.md) for the provider-specific parameters and requirements.

