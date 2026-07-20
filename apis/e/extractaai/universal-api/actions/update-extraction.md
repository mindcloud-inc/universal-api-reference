# Extracta.ai: Update Extraction

Updates an existing extraction in Extracta.ai.

```
PUT https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/update-extraction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extracta.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/update-extraction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extractionId": "string",
  "extractionDetails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extractaai/latest/actions/update-extraction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extractionId": "string",
    "extractionDetails": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extractionId` | string | yes | Unique identifier for the extraction. |
| `extractionDetails` | object | yes | Object containing the extraction fields to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extractionId": "string",
      "status": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extractionId` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Extracta.ai API, this operation is `PATCH /updateExtraction` (base URL `https://api.extracta.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-extraction.md) for the provider-specific parameters and requirements.

