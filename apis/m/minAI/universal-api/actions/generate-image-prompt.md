# 1minAI: Generate image prompt

Creates text prompts from uploaded images in 1minAI.

```
POST https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-image-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1minAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-image-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "images/2026_04_22_17_50_12_916_558123.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-image-prompt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "images/2026_04_22_17_50_12_916_558123.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Example: `images/2026_04_22_17_50_12_916_558123.png`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mode` | string | no | Default: `describe`. |
| `n` | number | no | Default: `1`. |

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

Through the native 1minAI API, this operation is `POST /api/features` (base URL `https://api.1min.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image-prompt.md) for the provider-specific parameters and requirements.

