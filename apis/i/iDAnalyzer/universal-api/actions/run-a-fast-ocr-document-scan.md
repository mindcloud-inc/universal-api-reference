# ID Analyzer: Run a fast OCR document scan

Creates a fast OCR document scan in ID Analyzer.

```
POST https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/run-a-fast-ocr-document-scan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ID Analyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/run-a-fast-ocr-document-scan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/run-a-fast-ocr-document-scan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | string | yes | Base64-encoded document image. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ID Analyzer API returns.

## Native endpoint

Through the native ID Analyzer API, this operation is `POST /quickscan` (base URL `https://api2.idanalyzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-a-fast-ocr-document-scan.md) for the provider-specific parameters and requirements.

