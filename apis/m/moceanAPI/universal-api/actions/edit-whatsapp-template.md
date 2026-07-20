# Mocean API: Edit WhatsApp Template



```
PUT https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/edit-whatsapp-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/edit-whatsapp-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/edit-whatsapp-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | no | Updated template category when allowed. |
| `components` | string | no | Updated JSON array string of template components. |
| `templateId` | string | yes | The WhatsApp template ID to edit. |

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

Through the native Mocean API API, this operation is `POST /template/whatsapp/:templateId` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-whatsapp-template.md) for the provider-specific parameters and requirements.

