# Kommunicate: Create Conversation With Assignee

Creates a new conversation with an assignee in Kommunicate.

```
POST https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/create-conversation-with-assignee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommunicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/create-conversation-with-assignee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupName": "Ava Chen",
  "groupMemberList[]": [
    "string"
  ],
  "assignee": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/create-conversation-with-assignee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupName": "Ava Chen",
    "groupMemberList[]": ["string"],
    "assignee": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupName` | string | yes | Conversation title. |
| `groupMemberList[]` | array<string> | yes | List of user, agent, or bot IDs to add to the conversation. |
| `assignee` | string | yes | Agent or bot ID to force-assign when skip routing is enabled. |
| `clientGroupId` | number | no | Optional client-generated conversation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminId": "string",
      "clientGroupId": "string",
      "createdAtTime": 1,
      "id": 1,
      "membersId": [
        "string"
      ],
      "metadata": {},
      "name": "Ava Chen",
      "updatedAtTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminId` | string |  |
| `clientGroupId` | string |  |
| `createdAtTime` | number |  |
| `id` | number |  |
| `membersId` | array<string> |  |
| `metadata` | object |  |
| `name` | string |  |
| `updatedAtTime` | number |  |

## Native endpoint

Through the native Kommunicate API, this operation is `POST /rest/ws/group/conversation` (base URL `https://services.kommunicate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversation-with-assignee.md) for the provider-specific parameters and requirements.

