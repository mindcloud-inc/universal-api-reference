# LoopedIn: Create Update

Creates a new update in LoopedIn.

```
POST https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "content": "string",
  "title": "string",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-update', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "content": "string",
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
| `category` | string | yes | The LoopedIn update category ID. |
| `content` | string | yes | The update content body. |
| `title` | string | yes | The update title. |
| `workspace_id` | string | yes | The LoopedIn workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "category": {},
      "created": "string",
      "dislikes": 1,
      "id": "string",
      "likes": 1,
      "neutrals": 1,
      "pinned": true,
      "public": true,
      "published": "string",
      "status": "string",
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
| `category` | object |  |
| `created` | string |  |
| `dislikes` | number |  |
| `id` | string |  |
| `likes` | number |  |
| `neutrals` | number |  |
| `pinned` | boolean |  |
| `public` | boolean |  |
| `published` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updated` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `POST /updates` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-update.md) for the provider-specific parameters and requirements.

