# LoopedIn: Create Idea

Creates a new idea in LoopedIn.

```
POST https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-idea" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "title": "string",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-idea', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "title": "string",
    "workspace_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | yes | The LoopedIn idea category ID. |
| `title` | string | yes | The idea title. |
| `workspace_id` | string | yes | The LoopedIn workspace ID. |

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
      "effort": 1,
      "followers": [
        {}
      ],
      "id": "string",
      "priority": 1,
      "public": true,
      "title": "string",
      "value": 1,
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
| `effort` | number |  |
| `followers` | array<object> |  |
| `id` | string |  |
| `priority` | number |  |
| `public` | boolean |  |
| `title` | string |  |
| `value` | number |  |
| `votes` | number |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `POST /ideas` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-idea.md) for the provider-specific parameters and requirements.

