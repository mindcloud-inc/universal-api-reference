# LoopedIn: Create Roadmap Card

Creates a new roadmap card in LoopedIn.

```
POST https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-roadmap-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-roadmap-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "column": "string",
  "objective": "string",
  "title": "string",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-roadmap-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "column": "string",
    "objective": "string",
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
| `column` | string | yes | The LoopedIn roadmap column ID. |
| `objective` | string | yes | The LoopedIn roadmap objective ID. |
| `title` | string | yes | The roadmap card title. |
| `workspace_id` | string | yes | The LoopedIn workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "archived": true,
      "column": {},
      "completed": true,
      "created": "string",
      "followers": [
        {}
      ],
      "id": "string",
      "jira": "string",
      "objective": {},
      "public": true,
      "roadmap": "string",
      "title": "string",
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
| `column` | object |  |
| `completed` | boolean |  |
| `created` | string |  |
| `followers` | array<object> |  |
| `id` | string |  |
| `jira` | string |  |
| `objective` | object |  |
| `public` | boolean |  |
| `roadmap` | string |  |
| `title` | string |  |
| `votes` | number |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `POST /roadmap-cards` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-roadmap-card.md) for the provider-specific parameters and requirements.

