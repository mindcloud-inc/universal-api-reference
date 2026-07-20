# Intercom: Attach Contact To Conversation



```
PUT https://connect.mindcloud.co/v1/universal/intercom/latest/actions/attach-contact-to-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/attach-contact-to-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "admin_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intercom/latest/actions/attach-contact-to-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "admin_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Intercom conversation identifier |
| `admin_id` | string | yes | Admin performing the action |
| `customer` | object | no |  |
| `customer.intercom_user_id` | string | no | Intercom contact ID to attach as a customer |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer.user_id` | string | no | Alternative provider user_id for customer identification |
| `customer.email` | string | no | Alternative customer email for identification |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {
          "id": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers` | array<object> |  |
| `customers[].id` | string |  |
| `customers[].type` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `POST /conversations/:conversation_id/customers` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-contact-to-conversation.md) for the provider-specific parameters and requirements.

