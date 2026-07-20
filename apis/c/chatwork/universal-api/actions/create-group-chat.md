# Chatwork: Create Group Chat



```
POST https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/create-group-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/create-group-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Website renewal project",
  "membersAdminIds": "123,542,1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/create-group-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Website renewal project",
    "membersAdminIds": "123,542,1001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the chat. Example: `Website renewal project`. |
| `membersAdminIds` | string | yes | Comma-separated account IDs for admin members. At least one account ID is required. Accepts multiple values in one string, delimited by `,`. Example: `123,542,1001`. |
| `membersMemberIds` | string | no | Comma-separated account IDs for member users. Accepts multiple values in one string, delimited by `,`. Example: `21,344`. |
| `membersReadonlyIds` | string | no | Comma-separated account IDs for read-only members. Accepts multiple values in one string, delimited by `,`. Example: `15,103`. |
| `description` | string | no | Summary of the chat. Example: `Project room for website renewal`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `iconPreset` | list<string> | no | Chat icon preset. One of: `beer`, `business`, `check`, `document`, `event`, `group`, `heart`, `idea`, `magcup`, `meeting`, `music`, `project`, `security`, `sports`, `star`, `study`, `travel`. |
| `link` | number | no | Whether to create an invitation link. Default: `0`. |
| `linkCode` | string | no | Path segment for the invitation link. Example: `project-room`. |
| `linkNeedAcceptance` | number | no | Whether admin approval is required to join through the invitation link. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "roomId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `roomId` | number |  |

## Native endpoint

Through the native Chatwork API, this operation is `POST /rooms` (base URL `https://api.chatwork.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group-chat.md) for the provider-specific parameters and requirements.

