# Chatnode: Get Leads



```
GET https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/get-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatnode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/get-leads?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatnode/latest/actions/get-leads?${params}`, {
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
| `botId` | string | yes | The Chatnode agent id associated with the trained agent model. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "enduser_email": "ava@example.com",
      "enduser_name": "Ava Chen",
      "enduser_phone": "string",
      "for_agent": true,
      "session_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Timestamp when the lead conversation was created. |
| `enduser_email` | string | End-user email associated with the lead. |
| `enduser_name` | string | End-user name associated with the lead. |
| `enduser_phone` | string | End-user phone associated with the lead. |
| `for_agent` | boolean | Whether the conversation has been transferred to a live agent. |
| `session_id` | string | Lead session identifier returned by Chatnode. |

## Native endpoint

Through the native Chatnode API, this operation is `POST get-conversation-ids/:botId` (base URL `https://api.public.chatnode.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leads.md) for the provider-specific parameters and requirements.

