# HITL Platform: List Loop Members



```
GET https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/list-loop-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HITL Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/list-loop-members?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/list-loop-members?${params}`, {
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
      "loop_id": "string",
      "member_count": 1,
      "members": [
        {
          "email": "ava@example.com",
          "joined_at": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "user_id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `loop_id` | string |  |
| `member_count` | number |  |
| `members[].email` | string |  |
| `members[].joined_at` | date |  |
| `members[].status` | string |  |
| `members[].user_id` | string |  |

## Native endpoint

Through the native HITL Platform API, this operation is `GET /api/loops/:id/members` (base URL `https://api.hitl.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-loop-members.md) for the provider-specific parameters and requirements.

