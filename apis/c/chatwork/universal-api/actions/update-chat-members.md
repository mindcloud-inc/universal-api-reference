# Chatwork: Update Chat Members



```
PUT https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "123456789",
  "membersAdminIds": "123,542,1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/update-chat-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "123456789",
    "membersAdminIds": "123,542,1001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes | Room ID. Example: `123456789`. |
| `membersAdminIds` | string | yes | Comma-separated account IDs for admin members. At least one account ID is required. Accepts multiple values in one string, delimited by `,`. Example: `123,542,1001`. |
| `membersMemberIds` | string | no | Comma-separated account IDs for member users. Accepts multiple values in one string, delimited by `,`. Example: `21,344`. |
| `membersReadonlyIds` | string | no | Comma-separated account IDs for read-only members. Accepts multiple values in one string, delimited by `,`. Example: `15,103`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": [
        1
      ],
      "member": [
        1
      ],
      "readonly": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | array<number> |  |
| `member` | array<number> |  |
| `readonly` | array<number> |  |

## Native endpoint

Through the native Chatwork API, this operation is `PUT /rooms/:room_id/members` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat-members.md) for the provider-specific parameters and requirements.

