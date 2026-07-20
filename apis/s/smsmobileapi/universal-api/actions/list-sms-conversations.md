# Smsmobileapi: List SMS Conversations

Retrieves SMS conversations from Smsmobileapi.

```
GET https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-sms-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smsmobileapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-sms-conversations?connectionId=$CONNECTION_ID&origineConversation=received" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "origineConversation": "received"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-sms-conversations?${params}`, {
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
| `origineConversation` | list | yes | Choose whether the conversation list is seeded from received or sent SMS logs. One of: `received`, `sent`. |
| `numero` | string | no | Filter to one specific phone number. |
| `date_from` | date | no | Only include conversations and messages from this date forward. |
| `date_to` | date | no | Only include conversations and messages up to this date. |
| `sort` | list | no | Sort the conversation list ascending or descending. One of: `ASC`, `DESC`. |
| `limit` | number | no | Maximum number of conversations to return when a phone number is not provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversations": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversations` | array<object> | Conversation rows grouped by phone number. |
| `success` | boolean | Whether the conversation lookup succeeded. |

## Native endpoint

Through the native Smsmobileapi API, this operation is `GET /conversation/sms/list/` (base URL `https://api.smsmobileapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sms-conversations.md) for the provider-specific parameters and requirements.

