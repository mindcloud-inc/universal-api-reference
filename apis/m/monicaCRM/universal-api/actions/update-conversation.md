# Monica CRM: Update Conversation

Updates an existing conversation in Monica CRM.

```
PUT https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monica CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "happenedAt": "2026-05-07T12:00:00.000Z",
  "contactFieldTypeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "happenedAt": "2026-05-07T12:00:00.000Z",
    "contactFieldTypeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes |  |
| `happenedAt` | date | yes |  |
| `contactFieldTypeId` | string | yes | The contact field type ID associated with the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contact_field_type": {
          "id": 1,
          "name": "Ava Chen"
        },
        "contact": {
          "complete_name": "Ava Chen",
          "id": 1
        },
        "created_at": "string",
        "happened_at": "string",
        "id": 1,
        "messages": [
          {}
        ],
        "object": "string",
        "updated_at": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.contact_field_type.id` | number |  |
| `data.contact_field_type.name` | string |  |
| `data.contact.complete_name` | string |  |
| `data.contact.id` | number |  |
| `data.created_at` | string |  |
| `data.happened_at` | string |  |
| `data.id` | number |  |
| `data.messages` | array<object> |  |
| `data.object` | string |  |
| `data.updated_at` | string |  |

## Native endpoint

Through the native Monica CRM API, this operation is `PUT /conversations/:conversationId` (base URL `https://app.monicahq.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

