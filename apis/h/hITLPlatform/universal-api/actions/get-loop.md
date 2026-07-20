# HITL Platform: Get Loop



```
GET https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/get-loop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HITL Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/get-loop?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/get-loop?${params}`, {
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
| `id` | string | yes | The unique identifier of the loop. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "loop": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "creator_id": "string",
        "description": "string",
        "icon": "string",
        "id": "string",
        "member_count": 1,
        "members": [
          {
            "email": "ava@example.com",
            "joined_at": "2026-05-07T12:00:00.000Z",
            "status": "string",
            "user_id": "string"
          }
        ],
        "name": "Ava Chen",
        "pending_count": 1,
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `loop.created_at` | date |  |
| `loop.creator_id` | string |  |
| `loop.description` | string |  |
| `loop.icon` | string |  |
| `loop.id` | string |  |
| `loop.member_count` | number |  |
| `loop.members[].email` | string |  |
| `loop.members[].joined_at` | date |  |
| `loop.members[].status` | string |  |
| `loop.members[].user_id` | string |  |
| `loop.name` | string |  |
| `loop.pending_count` | number |  |
| `loop.updated_at` | date |  |

## Native endpoint

Through the native HITL Platform API, this operation is `GET /api/loops/:id` (base URL `https://api.hitl.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-loop.md) for the provider-specific parameters and requirements.

