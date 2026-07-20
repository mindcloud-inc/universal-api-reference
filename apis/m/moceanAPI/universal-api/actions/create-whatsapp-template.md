# Mocean API: Create WhatsApp Template



```
POST https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/create-whatsapp-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/create-whatsapp-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "components": "string",
  "language": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/create-whatsapp-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "components": "string",
    "language": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowCategoryChange` | string | no | Allow Meta to reassign the category when needed. |
| `category` | string | yes | Template category. |
| `components` | string | yes | JSON array string describing template components. |
| `language` | string | yes | Template language code. |
| `messageTtlSeconds` | string | no | Optional authentication template TTL in seconds. |
| `name` | string | yes | Template name using lowercase letters, numbers, and underscores. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "components": [
        [
          {}
        ]
      ],
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `components[]` | array<object> |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Mocean API API, this operation is `POST /template/whatsapp/message_templates` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-whatsapp-template.md) for the provider-specific parameters and requirements.

