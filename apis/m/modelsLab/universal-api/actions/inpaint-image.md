# ModelsLab: Inpaint Image

Creates an inpainted image in ModelsLab.

```
POST https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/inpaint-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ModelsLab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/inpaint-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/inpaint-image', {
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
| `init_image` | string | no | Image URL to inpaint. |
| `mask_image` | string | no | Mask image URL for the inpainted region. |
| `prompt` | string | no | Prompt describing the masked-region fill. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generationTime": 1,
      "id": 1,
      "meta": {},
      "output": [
        "string"
      ],
      "proxy_links": [
        "https://example.com"
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
| `generationTime` | number |  |
| `id` | number |  |
| `meta` | object |  |
| `output` | array<string> |  |
| `proxy_links` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native ModelsLab API, this operation is `POST /v6/realtime/inpaint` (base URL `https://modelslab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inpaint-image.md) for the provider-specific parameters and requirements.

