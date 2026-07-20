# DeepImage: Business Avatar Generation

Creates a business avatar image in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/business-avatar-generation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/business-avatar-generation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://deep-image.ai/api-example3.jpg",
  "background.generate.description": "Woman in a beige pantsuit, arms in pockets, looking professional, standing near a bookshelf."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/business-avatar-generation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://deep-image.ai/api-example3.jpg",
    "background.generate.description": "Woman in a beige pantsuit, arms in pockets, looking professional, standing near a bookshelf."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the source face image. Example: `https://deep-image.ai/api-example3.jpg`. |
| `background.generate.description` | string | yes | Prompt describing the desired business portrait or avatar. Example: `Woman in a beige pantsuit, arms in pockets, looking professional, standing near a bookshelf.`. |
| `background.generate.face_id` | boolean | no | When enabled, DeepImage uses the documented `face_id` toggle to allow more changes to hair and similar details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageApp": "string",
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
| `imageApp` | string |  |
| `job` | string |  |
| `originalImg` | string |  |
| `queue` | number |  |

## Native endpoint

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/business-avatar-generation.md) for the provider-specific parameters and requirements.

