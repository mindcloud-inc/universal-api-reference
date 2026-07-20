# Templated: Create Render

Creates a new render in Templated.

```
POST https://connect.mindcloud.co/v1/universal/templated/latest/actions/create-render
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Templated `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/templated/latest/actions/create-render" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/templated/latest/actions/create-render', {
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
| `template` | string | no | The template id that you want to render. |
| `templates[]` | array<string> | no | Optional list of template ids for batch rendering. |
| `layers` | object | no | An object of layers that will be updated in the template. |
| `pages[]` | array<object> | no | Optional page-specific layer modifications for multi-page templates. |
| `format` | string | no | Render format: jpg, png, webp, pdf, or mp4. |
| `externalId` | string | no | External identifier to associate the render with an entity in your system. |
| `webhookUrl` | string | no | URL to POST the full render object to when rendering completes. |
| `async` | boolean | no | When true, create the render asynchronously. |
| `merge` | boolean | no | When true, merge multi-page template renders into a single PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "externalId": "string",
      "format": "string",
      "height": 1,
      "id": "string",
      "name": "Ava Chen",
      "page": "string",
      "payload": "string",
      "render_url": "https://example.com",
      "status": "string",
      "templateId": "string",
      "templateName": "Ava Chen",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `externalId` | string |  |
| `format` | string |  |
| `height` | number |  |
| `id` | string |  |
| `name` | string |  |
| `page` | string |  |
| `payload` | string |  |
| `render_url` | string |  |
| `status` | string |  |
| `templateId` | string |  |
| `templateName` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Templated API, this operation is `POST /v1/render` (base URL `https://api.templated.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-render.md) for the provider-specific parameters and requirements.

