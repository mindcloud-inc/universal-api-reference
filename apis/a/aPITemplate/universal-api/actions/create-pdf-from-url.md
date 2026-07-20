# API Template: Create PDF From URL

Creates a PDF from a URL in API Template.

```
POST https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-pdf-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a API Template `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-pdf-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/create-pdf-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | URL to convert into a PDF. |
| `settings` | object | no | Rendering settings for the generated PDF. |
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

Through the native API Template API, this operation is `POST /v2/create-pdf-from-url` (base URL `https://rest.apitemplate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf-from-url.md) for the provider-specific parameters and requirements.

