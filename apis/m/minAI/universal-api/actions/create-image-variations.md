# 1minAI: Create image variations

Creates image variations from an uploaded image in 1minAI.

```
POST https://connect.mindcloud.co/v1/universal/minAI/latest/actions/create-image-variations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1minAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minAI/latest/actions/create-image-variations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "images/2025_10_22_11_15_29_408_cat.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minAI/latest/actions/create-image-variations', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "images/2025_10_22_11_15_29_408_cat.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Example: `images/2025_10_22_11_15_29_408_cat.png`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list | no | One of: `JPG`, `PNG`, `WebP`. Default: `webp`. |
| `aspectRatio` | string | no | Default: `4:3`. |
| `numOutputs` | number | no | Default: `1`. |
| `numInferenceSteps` | number | no | Default: `4`. |
| `outputQuality` | number | no | Default: `80`. |
| `megapixels` | list | no | One of: `0.25 MP`, `1 MP`. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiRecord": {},
      "temporaryUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiRecord` | object |  |
| `temporaryUrl` | string |  |

## Native endpoint

Through the native 1minAI API, this operation is `POST /api/features` (base URL `https://api.1min.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image-variations.md) for the provider-specific parameters and requirements.

