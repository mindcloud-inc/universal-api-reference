# Ainoflow Convert: Submit Base64 Document

Creates a conversion job in Ainoflow Convert from base64 content.

```
POST https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-base64-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ainoflow Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-base64-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentBase64": "JVBERi0xLjQK...",
  "languages": "en,de",
  "outputs": "text,pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-base64-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentBase64": "JVBERi0xLjQK...",
    "languages": "en,de",
    "outputs": "text,pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentBase64` | string | yes | Base64-encoded file content. Example: `JVBERi0xLjQK...`. |
| `filename` | string | no | Original filename for content type detection. Example: `document.pdf`. |
| `languages` | string | yes | Comma-separated language codes. Accepts multiple values in one string, delimited by `,`. Example: `en,de`. |
| `outputs` | string | yes | Comma-separated output formats. Accepts multiple values in one string, delimited by `,`. Example: `text,pdf`. |
| `models` | string | no | Processing model (default: auto). Default: `auto`. |
| `response` | string | no | Response mode (default: polling). Default: `polling`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {
          "models": "string",
          "text": {
            "expiration": "string",
            "url": "https://example.com"
          }
        }
      ],
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
| `files` | array<object> |  |
| `files[].models` | string |  |
| `files[].text.expiration` | string |  |
| `files[].text.url` | string |  |
| `id` | string |  |
| `models` | string |  |
| `processingTimeInSeconds` | number |  |
| `reference` | string |  |
| `responseMode` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Ainoflow Convert API, this operation is `POST /api/v1/convert/submit-base64` (base URL `https://api.ainoflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-base64-document.md) for the provider-specific parameters and requirements.

