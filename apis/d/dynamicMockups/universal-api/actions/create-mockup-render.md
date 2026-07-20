# Dynamic Mockups: Create Mockup Render

Creates a mockup render in Dynamic Mockups.

```
POST https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-mockup-render
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Mockups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-mockup-render" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mockup_uuid": "e.g. 754a46c5-7693-43a1-9cd4-aedabd273f57",
  "smart_objects": "JSON array, e.g. [{\"uuid\":\"...\",\"asset\":{\"url\":\"https://...\"}}]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-mockup-render', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mockup_uuid": "e.g. 754a46c5-7693-43a1-9cd4-aedabd273f57",
    "smart_objects": "JSON array, e.g. [{\"uuid\":\"...\",\"asset\":{\"url\":\"https://...\"}}]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mockup_uuid` | string | yes | UUID of the mockup template to render. Example: `e.g. 754a46c5-7693-43a1-9cd4-aedabd273f57`. |
| `export_label` | string | no | Optional label returned back in render response. Example: `e.g. my-first-render`. |
| `export_options.image_format` | string | no | Optional export format: jpg, png, or webp. Example: `jpg \| png \| webp`. |
| `export_options.image_size` | number | no | Optional output width in pixels. Example: `e.g. 1200`. |
| `export_options.mode` | string | no | Optional mode: view or download. Example: `view \| download`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `smart_objects` | list<object> | yes | JSON array of smart object mappings (uuid + asset/text options). Example: `JSON array, e.g. [{"uuid":"...","asset":{"url":"https://..."}}]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "exportLabel": "string",
        "exportPath": "string"
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.exportLabel` | string |  |
| `data.exportPath` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Dynamic Mockups API, this operation is `POST api/v1/renders` (base URL `https://app.dynamicmockups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mockup-render.md) for the provider-specific parameters and requirements.

