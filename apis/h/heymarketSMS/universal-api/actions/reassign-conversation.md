# Heymarket SMS: Reassign Conversation



```
PUT https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/reassign-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/reassign-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": 1,
  "userId": 1,
  "reassignId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/reassign-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": 1,
    "userId": 1,
    "reassignId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | number | yes | Unique identifier of the inbox. |
| `userId` | number | yes | Unique identifier of the current user. |
| `reassignId` | number | yes | Unique identifier of the user to assign the conversation to. |
| `target` | string | no | Phone number for the conversation. |
| `targets[]` | array<string> | no | Phone numbers for a group MMS conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `POST /v1/conversations/reassign` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reassign-conversation.md) for the provider-specific parameters and requirements.

