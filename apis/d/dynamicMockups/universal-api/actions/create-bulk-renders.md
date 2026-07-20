# Dynamic Mockups: Create Bulk Renders

Creates bulk renders from a Dynamic Mockups collection.

```
POST https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-bulk-renders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Mockups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-bulk-renders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collection_uuid": "e.g. 0663101b-f01c-4e85-89af-f90b4e9f983b"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-bulk-renders', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collection_uuid": "e.g. 0663101b-f01c-4e85-89af-f90b4e9f983b"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collection_uuid` | string | yes | UUID of the Dynamic Mockups collection to bulk render. Example: `e.g. 0663101b-f01c-4e85-89af-f90b4e9f983b`. |
| `export_label` | string | no | Optional label returned back in bulk render response. Example: `e.g. fall-collection-render`. |
| `export_options.image_format` | string | no | Optional export format: jpg, png, or webp. Example: `jpg \| png \| webp`. |
| `export_options.image_size` | number | no | Optional output width in pixels. Example: `e.g. 1200`. |
| `export_options.mode` | string | no | Optional mode: view or download. Example: `view \| download`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `artworks` | object | no | JSON object mapping artwork input keys to image URLs or files. Example: `JSON object, e.g. {"artwork_main":"https://.../design.png"}`. |
| `colors` | object | no | JSON object mapping color input keys to hex color values. Example: `JSON object, e.g. {"color_main":"#C0375E"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dynamic Mockups API returns.

## Native endpoint

Through the native Dynamic Mockups API, this operation is `POST api/v1/renders/bulk` (base URL `https://app.dynamicmockups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-renders.md) for the provider-specific parameters and requirements.

