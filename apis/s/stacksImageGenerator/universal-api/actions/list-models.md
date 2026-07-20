# 88stacks Image Generator: List Models

Retrieves image generation models from 88stacks Image Generator.

```
GET https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 88stacks Image Generator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/list-models?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native 88stacks Image Generator API, this operation is `GET /api/v1/models` (base URL `https://api.88stacks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

