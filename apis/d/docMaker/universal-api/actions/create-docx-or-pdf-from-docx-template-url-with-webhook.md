# DocMaker: Create DOCX Or PDF from DOCX Template URL With Webhook

Creates a DOCX or PDF from a template URL with webhook in DocMaker.

```
POST https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-docx-or-pdf-from-docx-template-url-with-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocMaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-docx-or-pdf-from-docx-template-url-with-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "templateUrl": "https://example.com",
  "outputType": "string",
  "webhookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-docx-or-pdf-from-docx-template-url-with-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "templateUrl": "https://example.com",
    "outputType": "string",
    "webhookUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `templateUrl` | string | yes |  |
| `data` | object | no |  |
| `outputType` | string | yes |  |
| `webhookUrl` | string | yes |  |
| `metadata` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | DocMaker job identifier for the created document request |
| `status` | string | DocMaker job creation status |

## Native endpoint

Through the native DocMaker API, this operation is `POST /docx_fill_convert` (base URL `https://api.v2.docmaker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-docx-or-pdf-from-docx-template-url-with-webhook.md) for the provider-specific parameters and requirements.

