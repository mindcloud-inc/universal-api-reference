# Docmosis: Render Documents



```
POST https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/render-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/render-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateName": "/samples/WelcomeTemplate.docx",
  "outputName": "output.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/render-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateName": "/samples/WelcomeTemplate.docx",
    "outputName": "output.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateName` | string | yes | Name of the template to render. The template must already exist in Docmosis. Example: `/samples/WelcomeTemplate.docx`. |
| `outputName` | string | yes | Filename for the rendered document output. The extension can imply the format when Output Format is omitted. Example: `output.pdf`. |
| `data` | object | no | Structured JSON data merged into the template. Example: `[object Object]`. |
| `streamResultInResponse` | boolean | no | When true, base64-encodes the streamed result into the JSON response body. |
| `outputFormat` | string | no | Optional output format. Valid options are PDF, DOCX, ODT, or TXT. Example: `PDF`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storeTo` | string | no | Optional destination for the rendered output such as stream, mailto, or s3. Defaults to streaming the result back. Example: `stream`. |
| `requestId` | string | no | Optional caller-provided identifier echoed back in the response. Example: `invoice-123`. |
| `tags` | string | no | Semicolon-separated tags to record against this render for later reporting. |
| `devMode` | string | no | If set to y, yes, or true, render in development mode instead of failing hard on template/data issues. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "queue": {
        "availablePct": 1,
        "delaySeconds": 1,
        "rejected": true
      },
      "resultFile": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `queue.availablePct` | number | Approximate queue availability percentage reported by Docmosis. |
| `queue.delaySeconds` | number | Estimated queue delay in seconds. |
| `queue.rejected` | boolean | Whether the Docmosis queue rejected the render request. |
| `resultFile` | string | Base64-encoded rendered document when Stream Result In Response is true. |
| `succeeded` | boolean | Whether the render request succeeded. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /render` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-documents.md) for the provider-specific parameters and requirements.

