# Invoice Ninja: Update Client



```
PUT https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "name": "Ava Chen",
  "countryId": "840",
  "contacts[0].first_name": "Ava",
  "contacts[0].last_name": "Chen",
  "contacts[0].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "name": "Ava Chen",
    "countryId": "840",
    "contacts[0].first_name": "Ava",
    "contacts[0].last_name": "Chen",
    "contacts[0].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | Hashed client ID from Invoice Ninja. |
| `name` | string | yes | Updated client company or organization name. |
| `countryId` | number | yes | Country identifier required by Invoice Ninja when updating a client. Example: `840`. |
| `contacts[0].first_name` | string | yes | Primary contact first name. Invoice Ninja expects contacts to be sent on client updates. |
| `contacts[0].last_name` | string | yes | Primary contact last name. Invoice Ninja expects contacts to be sent on client updates. |
| `contacts[0].email` | string | yes | Primary contact email. Invoice Ninja expects contacts to be sent on client updates. |
| `publicNotes` | string | no | Optional public notes shown on client-facing documents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "contacts": [
        {}
      ],
      "country_id": "string",
      "created_at": 1,
      "display_name": "Ava Chen",
      "documents": [
        {}
      ],
      "has_valid_vat_number": true,
      "id": "string",
      "is_deleted": true,
      "is_tax_exempt": true,
      "locations": [
        {}
      ],
      "name": "Ava Chen",
      "number": "string",
      "public_notes": "string",
      "settings": {},
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | Outstanding balance for the client. |
| `contacts` | array<object> | Client contact records returned by Invoice Ninja. |
| `country_id` | string | Country identifier. |
| `created_at` | number | Unix timestamp when the client was created. |
| `display_name` | string | Display label for the client. |
| `documents` | array<object> | Documents attached to the client. |
| `has_valid_vat_number` | boolean | Whether the VAT number is valid. |
| `id` | string | Hashed client ID. |
| `is_deleted` | boolean | Whether the client is deleted. |
| `is_tax_exempt` | boolean | Whether the client is tax exempt. |
| `locations` | array<object> | Locations associated with the client. |
| `name` | string | Client company or organization name. |
| `number` | string | Client number. |
| `public_notes` | string | Public notes shown on client-facing documents. |
| `settings` | object | Client-level settings object. |
| `updated_at` | number | Unix timestamp when the client was last updated. |

## Native endpoint

Through the native Invoice Ninja API, this operation is `PUT /clients/:id` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

