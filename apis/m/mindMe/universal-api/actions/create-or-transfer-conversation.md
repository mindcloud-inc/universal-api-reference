# MindMe: Create Or Transfer Conversation

Creates or transfers a conversation in MindMe.

```
POST https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/create-or-transfer-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/create-or-transfer-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/create-or-transfer-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | no |  |
| `email` | string | no |  |
| `firstName` | string | no |  |
| `inboxId` | string | no |  |
| `isSendMessage` | string | no |  |
| `lastName` | string | no |  |
| `messageBody` | string | no |  |
| `mobileNumber` | string | no |  |
| `parentAccountId` | string | no |  |
| `sendOption` | string | no |  |
| `subAccountId` | string | no |  |
| `userId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MindMe API returns.

## Native endpoint

Through the native MindMe API, this operation is `POST /api/Conversation/CreateOrTransferConversation` (base URL `https://prodapi.mindmemobile.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-transfer-conversation.md) for the provider-specific parameters and requirements.

