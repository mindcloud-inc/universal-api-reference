# LoopedIn: Create Feedback

Creates a new feedback item in LoopedIn.

```
POST https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "board": "string",
  "category": "string",
  "title": "string",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "board": "string",
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
| `board` | string | yes | The LoopedIn feedback board ID. |
| `category` | string | yes | The LoopedIn feedback category ID. |
| `title` | string | yes | The feedback title. |
| `workspace_id` | string | yes | The LoopedIn workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "board": "string",
      "category": "string",
      "completed": true,
      "created": "string",
      "createdBy": "string",
      "description": "string",
      "id": "string",
      "public": true,
      "title": "string",
      "updated": "string",
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
| `board` | string |  |
| `category` | string |  |
| `completed` | boolean |  |
| `created` | string |  |
| `createdBy` | string |  |
| `description` | string |  |
| `id` | string |  |
| `public` | boolean |  |
| `title` | string |  |
| `updated` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `POST /feedback` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feedback.md) for the provider-specific parameters and requirements.

