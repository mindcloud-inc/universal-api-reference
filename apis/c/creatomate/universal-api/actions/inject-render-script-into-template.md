# Creatomate: Inject RenderScript Into Template

Creates a render by injecting RenderScript into a template.

```
POST https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/inject-render-script-into-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creatomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/inject-render-script-into-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "YOUR_TEMPLATE_ID_HERE",
  "videoUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/inject-render-script-into-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "YOUR_TEMPLATE_ID_HERE",
    "videoUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Creatomate template ID to render from. Example: `YOUR_TEMPLATE_ID_HERE`. |
| `compositionName` | string | no | Template composition whose `elements` array should be replaced or appended. Default: `Video-Composition`. Example: `Video-Composition`. |
| `videoUrls[]` | array<string> | yes | Ordered list of video URLs to inject into the target composition. |
| `appendToExisting` | boolean | no | Whether to append the videos to the existing composition instead of replacing it. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "outputFormat": "string",
      "snapshotUrl": "https://example.com",
      "status": "string",
      "templateId": "string",
      "templateName": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Creatomate render ID. |
| `outputFormat` | string | Output format requested for the render. |
| `snapshotUrl` | string | Preview image URL returned for the render. |
| `status` | string | Current render status returned by Creatomate. |
| `templateId` | string | Creatomate template ID used for the render. |
| `templateName` | string | Template name returned by Creatomate. |
| `url` | string | Direct URL for the rendered output file. |

## Native endpoint

Through the native Creatomate API, this operation is `POST /v2/renders` (base URL `https://api.creatomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inject-render-script-into-template.md) for the provider-specific parameters and requirements.

