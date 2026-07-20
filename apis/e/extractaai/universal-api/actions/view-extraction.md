# Extracta.ai: View Extraction

Retrieves an extraction from Extracta.ai.

```
GET https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/view-extraction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/view-extraction?connectionId=$CONNECTION_ID&extractionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extractionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/view-extraction?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "extractionDetails": {},
      "extractionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extractionDetails` | object |  |
| `extractionId` | string |  |

## Native endpoint

Through the native Extracta.ai API, this operation is `POST /viewExtraction` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-extraction.md) for the provider-specific parameters and requirements.

