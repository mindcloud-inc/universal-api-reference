# Templated: Duplicate Render

Duplicates an existing render in Templated.

```
POST https://connect.mindcloud.co/v1/universal/templated/latest/actions/duplicate-render
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Templated `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/templated/latest/actions/duplicate-render" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "renderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/templated/latest/actions/duplicate-render', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "renderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `renderId` | string | yes | The render id of the render that you want to duplicate. |

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

Through the native Templated API, this operation is `POST /v1/render/:id/duplicate` (base URL `https://api.templated.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-render.md) for the provider-specific parameters and requirements.

