# NiftyImages: Update Photoshop Image Layers

Updates Photoshop image layers in NiftyImages.

```
PUT https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/update-photoshop-image-layers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/update-photoshop-image-layers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "Layers[]": [
    {}
  ],
  "Layers[].LayerName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/update-photoshop-image-layers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "Layers[]": [{}],
    "Layers[].LayerName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | NiftyImages image URL. |
| `Name` | string | no | Name of the image. |
| `Variables[]` | array<object> | no | Variables array. |
| `Variables[].Name` | string | no | Variable or placeholder name. |
| `Variables[].DefaultValue` | string | no | Default value for the variable. |
| `Layers[]` | array<object> | yes | PSD layers to update. |
| `Layers[].LayerName` | string | yes | Layer name. |
| `Layers[].TextValue` | string | no | Text value to apply to the layer. |
| `Layers[].TextColor` | string | no | Color to apply to the layer. |
| `Layers[].ImageUrl` | string | no | Image URL for smart object layer updates. |
| `Layers[].Show` | boolean | no | Set to true to show the layer or false to hide it. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Hide": true,
      "LayerName": "Ava Chen",
      "TextColor": "string",
      "TextValue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Hide` | boolean |  |
| `LayerName` | string |  |
| `TextColor` | string |  |
| `TextValue` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `PUT /Psd` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-photoshop-image-layers.md) for the provider-specific parameters and requirements.

