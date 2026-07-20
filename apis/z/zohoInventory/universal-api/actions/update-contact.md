# Zoho Inventory: Update Contact

Updates an existing contact in Zoho Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "organizationId": "{{credentials.organizationId}}",
  "contactName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "organizationId": "{{credentials.organizationId}}",
    "contactName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The Zoho Inventory contact_id for the contact. |
| `organizationId` | string | yes | Zoho Inventory organization ID to run this request against. Default: `{{credentials.organizationId}}`. |
| `contactName` | string | yes | The display name for the contact. |
| `contactType` | string | no | Whether the contact is a customer or vendor. Default: `customer`. |
| `companyName` | string | no | Company name for a business contact. |
| `notes` | string | no | Internal notes for the contact. |
| `contactPersons[]` | array<object> | no | One or more contact people associated with this contact. |
| `contactPersons[].firstName` | string | no | First name of the contact person. |
| `contactPersons[].lastName` | string | no | Last name of the contact person. |
| `contactPersons[].email` | string | no | Email address for the contact person. |
| `contactPersons[].phone` | string | no | Phone number for the contact person. |
| `contactPersons[].isPrimaryContact` | boolean | no | Whether this is the primary contact person. |

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

Through the native Zoho Inventory API, this operation is `PUT /contacts/:contact_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

