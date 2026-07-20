# API Template: Create PDF

Creates a PDF in API Template.

```
POST https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Template `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template ID to render. |
| `exportType` | string | no | Return the output as JSON metadata or a file response. |
| `expiration` | number | no | Minutes before the generated file expires; use 0 to store permanently. |
| `outputFormat` | string | no | Output format for the generated PDF. |
| `filename` | string | no | Filename for the generated file. |
| `cloudStorage` | number | no | Whether to upload the generated file to APITemplate cloud storage. |
| `asyncMode` | string | no | Generate the file asynchronously. |
| `webhookUrl` | string | no | Webhook URL for async completion notifications. |
| `webhookMethod` | string | no | HTTP method for the webhook callback. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native API Template API returns.

## Native endpoint

Through the native API Template API, this operation is `POST /v2/create-pdf` (base URL `https://rest.apitemplate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf.md) for the provider-specific parameters and requirements.

