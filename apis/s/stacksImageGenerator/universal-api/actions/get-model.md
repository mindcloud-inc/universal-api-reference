# 88stacks Image Generator: Get Model

Retrieves an image generation model from 88stacks Image Generator.

```
GET https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 88stacks Image Generator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/get-model?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/get-model?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the model to retrieve. |

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

Through the native 88stacks Image Generator API, this operation is `GET /api/v1/models/:id` (base URL `https://api.88stacks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

