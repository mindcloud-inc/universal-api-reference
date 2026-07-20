# DeepImage: Accurate Business Avatar

Creates an accurate business avatar in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/accurate-business-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/accurate-business-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://deep-image.ai/api-example3.jpg",
  "background.generate.description": "A woman sitting behind a desk in a modern office environment. Her smiling face is seen from behind her computer screen, with only the top of her head and a portion of her shoulders visible. The office space around her is bright and airy, illuminated by soft, natural light streaming in from large windows."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/accurate-business-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://deep-image.ai/api-example3.jpg",
    "background.generate.description": "A woman sitting behind a desk in a modern office environment. Her smiling face is seen from behind her computer screen, with only the top of her head and a portion of her shoulders visible. The office space around her is bright and airy, illuminated by soft, natural light streaming in from large windows."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the source face image. Example: `https://deep-image.ai/api-example3.jpg`. |
| `background.generate.description` | string | yes | Prompt describing the desired accurate business portrait. Example: `A woman sitting behind a desk in a modern office environment. Her smiling face is seen from behind her computer screen, with only the top of her head and a portion of her shoulders visible. The office space around her is bright and airy, illuminated by soft, natural light streaming in from large windows.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `background.generate.model_type` | string | no | Generative model used for avatar creation. Default: `google-gemini-image-flash`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageApp": {},
      "job": "string",
      "originalImg": "string",
      "queue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageApp` | object |  |
| `job` | string |  |
| `originalImg` | string |  |
| `queue` | number |  |

## Native endpoint

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accurate-business-avatar.md) for the provider-specific parameters and requirements.

