# LoopedIn: Get Feedback

Retrieves a feedback item from LoopedIn.

```
GET https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-feedback?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-feedback?${params}`, {
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
| `id` | string | yes | The LoopedIn feedback ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "archived": true,
      "category": {},
      "completed": true,
      "created": "string",
      "createdBy": "string",
      "description": "string",
      "followers": [
        {}
      ],
      "id": "string",
      "public": true,
      "title": "string",
      "updated": "string",
      "votes": 1,
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `archived` | boolean |  |
| `category` | object |  |
| `completed` | boolean |  |
| `created` | string |  |
| `createdBy` | string |  |
| `description` | string |  |
| `followers` | array<object> |  |
| `id` | string |  |
| `public` | boolean |  |
| `title` | string |  |
| `updated` | string |  |
| `votes` | number |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `GET /feedback/:id` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feedback.md) for the provider-specific parameters and requirements.

