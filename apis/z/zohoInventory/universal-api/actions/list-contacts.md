# Zoho Inventory: List Contacts

Retrieves contacts from Zoho Inventory.

```
GET https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/list-contacts?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/list-contacts?${params}`, {
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
| `organizationId` | string | yes | The Zoho Inventory organization_id for the request. Default: `{{credentials.organizationId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "contact_id": "string",
      "contact_name": "Ava Chen",
      "contact_persons": [
        {}
      ],
      "contact_type": "string",
      "created_time": "string",
      "currency_code": "string",
      "email": "ava@example.com",
      "last_modified_time": "string",
      "notes": "string",
      "phone": "string",
      "primary_contact_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `contact_id` | string |  |
| `contact_name` | string |  |
| `contact_persons` | array<object> |  |
| `contact_type` | string |  |
| `created_time` | string |  |
| `currency_code` | string |  |
| `email` | string |  |
| `last_modified_time` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `primary_contact_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Inventory API, this operation is `GET /contacts` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

