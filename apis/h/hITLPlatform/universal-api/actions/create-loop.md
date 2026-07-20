# HITL Platform: Create Loop



```
POST https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/create-loop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HITL Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/create-loop" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/create-loop', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Description shown to loop members. |
| `icon` | string | no | Icon name for the loop. |
| `name` | string | yes | Name of the loop to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invite_code": "string",
      "join_url": "https://example.com",
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
      },
      "qr_code_base64": "string",
      "qr_code_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invite_code` | string |  |
| `join_url` | string |  |
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
| `qr_code_base64` | string |  |
| `qr_code_url` | string |  |

## Native endpoint

Through the native HITL Platform API, this operation is `POST /api/loops` (base URL `https://api.hitl.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-loop.md) for the provider-specific parameters and requirements.

