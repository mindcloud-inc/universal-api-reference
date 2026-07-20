# Creatomate: Rearrange Scenes In Template

Creates a render with rearranged template scenes in Creatomate.

```
POST https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/rearrange-scenes-in-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creatomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/rearrange-scenes-in-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "YOUR_TEMPLATE_ID_HERE",
  "sceneCopies[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/rearrange-scenes-in-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "YOUR_TEMPLATE_ID_HERE",
    "sceneCopies[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Creatomate template ID to render from. Example: `YOUR_TEMPLATE_ID_HERE`. |
| `sceneCopies[]` | array<object> | yes | Ordered scene copy instructions. Each object should include a `copy` scene name and any per-scene modifications from the template. |

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

Through the native Creatomate API, this operation is `POST /v2/renders` (base URL `https://api.creatomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rearrange-scenes-in-template.md) for the provider-specific parameters and requirements.

