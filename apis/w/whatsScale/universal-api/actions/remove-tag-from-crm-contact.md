# WhatsScale: Remove Tag from CRM Contact

Removes a tag from an existing WhatsScale CRM contact.

```
PUT https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/remove-tag-from-crm-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/remove-tag-from-crm-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/remove-tag-from-crm-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "tag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | CRM contact ID. |
| `tag` | string | yes | Tag to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "source": "string",
      "tags": [
        "string"
      ],
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `source` | string |  |
| `tags` | array<string> |  |
| `updated_at` | string |  |

## Native endpoint

Through the native WhatsScale API, this operation is `DELETE /api/crm/contacts/:id/tags/:tag` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag-from-crm-contact.md) for the provider-specific parameters and requirements.

