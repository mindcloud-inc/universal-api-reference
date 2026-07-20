# ThriveDesk: Get Customer Conversation



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-customer-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-customer-conversation?connectionId=$CONNECTION_ID&conversationId=string&customerEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string",
  "customerEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-customer-conversation?${params}`, {
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
| `conversationId` | string | yes | ThriveDesk customer conversation ID. |
| `customerEmail` | string | yes | Customer email address for the conversation lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Customer conversation details. |
| `message` | string | Error or result message. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/customer/conversations/{{conversationId}}` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-conversation.md) for the provider-specific parameters and requirements.

