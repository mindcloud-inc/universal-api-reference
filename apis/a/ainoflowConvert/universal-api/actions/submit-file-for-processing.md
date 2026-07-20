# Ainoflow Convert: Submit File for Processing

Creates a conversion job in Ainoflow Convert from an uploaded file.

```
POST https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-file-for-processing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ainoflow Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-file-for-processing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "languages": "en,de,fr",
  "outputs": "text,pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-file-for-processing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "languages": "en,de,fr",
    "outputs": "text,pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Document or audio file to process. |
| `languages` | string | yes | Comma-separated language codes. Accepts multiple values in one string, delimited by `,`. Example: `en,de,fr`. |
| `outputs` | string | yes | Comma-separated output formats. Accepts multiple values in one string, delimited by `,`. Example: `text,pdf`. |
| `models` | string | no | Processing model (auto, tesseract, paddleocr, whisper*). Default: `auto`. |
| `ocr` | string | no | OCR control (auto, force, skip). Default: `auto`. |
| `webhookUrl` | string | no | Optional webhook URL for completion notifications. |
| `reference` | string | no | Optional client reference ID for tracking. |
| `jobExpiryInMinutes` | number | no | Optional job expiration time in minutes. Default: `1440`. |
| `response` | string | no | Response mode (polling, direct, webhook, persisted). Default: `polling`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "models": "string",
      "processingTimeInSeconds": 1,
      "reference": "string",
      "responseMode": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `models` | string |  |
| `processingTimeInSeconds` | number |  |
| `reference` | string |  |
| `responseMode` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Ainoflow Convert API, this operation is `POST /api/v1/convert/submit-file` (base URL `https://api.ainoflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-file-for-processing.md) for the provider-specific parameters and requirements.

