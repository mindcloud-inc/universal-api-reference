# Umbler Talk: List Chat Relative Messages

Retrieves chat messages around a selected date in Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-chat-relative-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-chat-relative-messages?connectionId=$CONNECTION_ID&chatId=string&direction=string&fromEventUTC=2026-05-07T12%3A00%3A00.000Z&organizationId=string&take=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string",
  "direction": "string",
  "fromEventUTC": "2026-05-07T12:00:00.000Z",
  "organizationId": "string",
  "take": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/list-chat-relative-messages?${params}`, {
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
| `chatId` | string | yes | The chat ID. |
| `direction` | string | yes | Relative message direction. |
| `fromEventUTC` | date | yes | Start date/time for relative messages. |
| `organizationId` | string | yes | The organization ID. |
| `take` | number | yes | Number of messages to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMessagesBeforeAllowedOrganizationPlan": true,
      "messages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMessagesBeforeAllowedOrganizationPlan` | boolean |  |
| `messages` | array<object> |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/chats/[:chatId]/relative-messages/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-relative-messages.md) for the provider-specific parameters and requirements.

