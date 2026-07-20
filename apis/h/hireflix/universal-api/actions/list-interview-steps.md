# Hireflix: List Interview Steps

Retrieves steps for an interview in Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-interview-steps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-interview-steps?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-interview-steps?${params}`, {
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
| `variables.id` | string | yes | The Hireflix interview ID. |
| `variables.stepId` | string | no | Optionally limit the response to one interview step ID. |
| `variables.stepIndex` | number | no | Optionally limit the response to one interview step index. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__typename": "Ava Chen",
      "completed": true,
      "completedAt": 1,
      "description": "string",
      "id": "string",
      "index": 1,
      "question": {
        "createdAt": 1,
        "id": "string",
        "thumbnail": "string",
        "type": "string",
        "url": "https://example.com"
      },
      "retakes": 1,
      "timeToAnswer": 1,
      "timeToThink": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__typename` | string |  |
| `completed` | boolean |  |
| `completedAt` | number |  |
| `description` | string |  |
| `id` | string |  |
| `index` | number |  |
| `question.createdAt` | number |  |
| `question.id` | string |  |
| `question.thumbnail` | string |  |
| `question.type` | string |  |
| `question.url` | string |  |
| `retakes` | number |  |
| `timeToAnswer` | number |  |
| `timeToThink` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-interview-steps.md) for the provider-specific parameters and requirements.

