# DynaPictures: Generate Multipage PDF

Creates a PDF from a multipage DynaPictures template.

```
POST https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/generate-multipage-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynaPictures `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/generate-multipage-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/generate-multipage-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pages[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | string | no | Custom metadata for generated PDF pages. |
| `pages[]` | array<object> | yes | Pages to render in the batch PDF. |
| `pages[].layers[]` | array<object> | no | Layer customizations for the page. |
| `pages[].layers[].backgroundColor` | string | no | Background color of the layer. |
| `pages[].layers[].borderColor` | string | no | Border color of the layer. |
| `pages[].layers[].borderRadius` | string | no | Border radius of the layer. |
| `pages[].layers[].borderWidth` | string | no | Border width of the layer. |
| `pages[].layers[].color` | string | no | Text color for the layer. |
| `pages[].layers[].imageAlignH` | string | no | Horizontal alignment when imagePosition is align. |
| `pages[].layers[].imageAlignV` | string | no | Vertical alignment when imagePosition is align. |
| `pages[].layers[].imageEffect` | string | no | CSS filter-style effect applied to the image. |
| `pages[].layers[].imagePosition` | string | no | Positioning mode for the image inside its container. |
| `pages[].layers[].imageUrl` | string | no | Image used for an image layer. |
| `pages[].layers[].name` | string | no | Name of the layer to customize. |
| `pages[].layers[].opacity` | number | no | Layer opacity from 0 to 1. |
| `pages[].layers[].text` | string | no | Text rendered in the layer. |
| `pages[].metadata` | string | no | Custom metadata for this page. |
| `pages[].templateId` | string | no | Template ID to use for this page. |
| `templateId` | string | no | Default template ID for batch pages. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynaPictures API returns.

## Native endpoint

Through the native DynaPictures API, this operation is `POST /batch` (base URL `https://api.dynapictures.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-multipage-pdf.md) for the provider-specific parameters and requirements.

