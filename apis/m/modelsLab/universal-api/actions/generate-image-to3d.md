# ModelsLab: Generate Image To 3D

Creates a 3D asset from an image in ModelsLab.

```
POST https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/generate-image-to3d
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ModelsLab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/generate-image-to3d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/generate-image-to3d', {
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
| `init_image` | string | no | Source image URL for 3D generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eta": 1,
      "fetch_result": "string",
      "id": 1,
      "message": "string",
      "output": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eta` | number |  |
| `fetch_result` | string |  |
| `id` | number |  |
| `message` | string |  |
| `output` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native ModelsLab API, this operation is `POST /v6/3d/image_to_3d` (base URL `https://modelslab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image-to3d.md) for the provider-specific parameters and requirements.

