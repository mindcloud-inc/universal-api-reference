# 88stacks Image Generator: Create Model

Creates a new image generation model in 88stacks Image Generator.

```
POST https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/create-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 88stacks Image Generator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/create-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/create-model', {
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
| `name` | string | no | Name to assign to the model. |
| `description` | string | no | Description of the model. |
| `test` | string | no | Set this when you want to create a test model. |
| `trainingLink` | string | no | URL to a zip file of training images. |
| `promptsLink` | string | no | URL to a file containing prompts for training. |
| `images` | list<string> | no | One or more JPG images to upload directly for training. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callback": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "instancePrompt": "string",
      "invokesCount": 1,
      "keyword": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callback` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `instancePrompt` | string |  |
| `invokesCount` | number |  |
| `keyword` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native 88stacks Image Generator API, this operation is `POST /api/v1/models` (base URL `https://api.88stacks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-model.md) for the provider-specific parameters and requirements.

