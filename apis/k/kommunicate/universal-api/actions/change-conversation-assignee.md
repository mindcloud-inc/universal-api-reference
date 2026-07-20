# Kommunicate: Change Conversation Assignee

Updates a conversation assignee in Kommunicate.

```
PUT https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/change-conversation-assignee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommunicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/change-conversation-assignee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "assignee": "string",
  "ofUserId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/change-conversation-assignee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "assignee": "string",
    "ofUserId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Conversation identifier to update. |
| `assignee` | string | yes | Human agent email or ID to assign to the conversation. |
| `sendNotifyMessage` | boolean | no | Whether Kommunicate should send a notification message; defaults to true. |
| `takeOverFromBot` | boolean | no | Remove bots from the conversation when true. |
| `ofUserId` | string | yes | Admin or agent user ID to route into the required Of-User-Id header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generatedAt": 1,
      "response": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generatedAt` | number | Provider-generated timestamp. |
| `response` | string | Provider response message. |
| `status` | string | Provider operation status. |

## Native endpoint

Through the native Kommunicate API, this operation is `PATCH /rest/ws/group/assignee/change` (base URL `https://services.kommunicate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-conversation-assignee.md) for the provider-specific parameters and requirements.

