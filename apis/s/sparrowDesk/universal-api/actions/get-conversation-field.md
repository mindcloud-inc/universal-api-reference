# SparrowDesk: Get Conversation Field

Retrieves a conversation field from SparrowDesk.

```
GET https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-conversation-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-conversation-field?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-conversation-field?${params}`, {
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
| `id` | number | yes | SparrowDesk conversation field ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "description": "string",
      "fieldOptions": [
        {}
      ],
      "id": 1,
      "internalName": "Ava Chen",
      "isActive": true,
      "isDefault": true,
      "isMandatoryOnClose": true,
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Creation timestamp. |
| `description` | string | Field description. |
| `fieldOptions` | array<object> | Selectable field options. |
| `id` | number | Conversation field ID. |
| `internalName` | string | Internal field key. |
| `isActive` | boolean | Whether the field is active. |
| `isDefault` | boolean | Whether the field is a default field. |
| `isMandatoryOnClose` | boolean | Whether the field is required when closing a conversation. |
| `name` | string | Field label. |
| `type` | string | Field type. |
| `updatedAt` | number | Last update timestamp. |

## Native endpoint

Through the native SparrowDesk API, this operation is `GET /conversations/fields/{{id}}` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-field.md) for the provider-specific parameters and requirements.

