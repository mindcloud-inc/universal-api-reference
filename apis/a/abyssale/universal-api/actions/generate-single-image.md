# Abyssale: Generate Single Image

Generates a single image in Abyssale.

```
POST https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/generate-single-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abyssale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/generate-single-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designId": "46d22c62-d134-44d3-a040-138e4ea9ea08",
  "elements": "[object Object]",
  "template_format_name": "main-crisp"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/generate-single-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designId": "46d22c62-d134-44d3-a040-138e4ea9ea08",
    "elements": "[object Object]",
    "template_format_name": "main-crisp"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `designId` | string | yes | Design ID to generate from Example: `46d22c62-d134-44d3-a040-138e4ea9ea08`. |
| `elements` | object | yes | Customization payload for design elements Example: `[object Object]`. |
| `template_format_name` | string | yes | Format name to generate Example: `main-crisp`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abyssale API returns.

## Native endpoint

Through the native Abyssale API, this operation is `POST /banner-builder/:designId/generate` (base URL `https://api.abyssale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-single-image.md) for the provider-specific parameters and requirements.

