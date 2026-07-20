# Ainoflow Convert: Submit External URL

Creates a conversion job in Ainoflow Convert from an external URL.

```
POST https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-external-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ainoflow Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-external-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://example.com/document.pdf",
  "languages": "en,de",
  "outputs": "text,pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ainoflowConvert/latest/actions/submit-external-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://example.com/document.pdf",
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
| `sourceUrl` | string | yes | URL to download the file from. Example: `https://example.com/document.pdf`. |
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

Through the native Ainoflow Convert API, this operation is `POST /api/v1/convert/submit-url` (base URL `https://api.ainoflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-external-url.md) for the provider-specific parameters and requirements.

