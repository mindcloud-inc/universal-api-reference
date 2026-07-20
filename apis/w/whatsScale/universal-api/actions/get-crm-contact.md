# WhatsScale: Get CRM Contact

Retrieves a CRM contact from WhatsScale.

```
GET https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/get-crm-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/get-crm-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/get-crm-contact?${params}`, {
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
| `id` | string | yes | CRM contact ID. |

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

Through the native WhatsScale API, this operation is `GET /api/crm/contacts/:id` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crm-contact.md) for the provider-specific parameters and requirements.

