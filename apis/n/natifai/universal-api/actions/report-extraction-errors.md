# Natif.ai: Report Extraction Errors

Creates an extraction error report for Natif.ai processing.

```
POST https://connect.mindcloud.co/v1/universal/natifai/latest/actions/report-extraction-errors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/report-extraction-errors" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "processingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/natifai/latest/actions/report-extraction-errors', {
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
| `description` | string | no | Free-text description of the extraction error. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `incorrectFields[]` | array<object> | no | List of incorrect extraction fields, when known. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created extraction error report ID. |

## Native endpoint

Through the native Natif.ai API, this operation is `POST /processing/error-reports/extractions` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/report-extraction-errors.md) for the provider-specific parameters and requirements.

