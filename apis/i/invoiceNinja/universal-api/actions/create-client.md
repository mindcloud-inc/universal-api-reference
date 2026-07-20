# Invoice Ninja: Create Client



```
POST https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "countryId": "840",
  "contacts[0].first_name": "Ava",
  "contacts[0].last_name": "Chen",
  "contacts[0].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `include` | string | no | Optional related resources to include, comma separated. |
| `name` | string | yes | The name of the client company or organization. |
| `countryId` | number | yes | Country identifier required by the Invoice Ninja client schema. Example: `840`. |
| `contacts[0].first_name` | string | yes | First name for the primary contact. Client contacts must be included on mutating requests. |
| `contacts[0].last_name` | string | yes | Last name for the primary contact. Client contacts must be included on mutating requests. |
| `contacts[0].email` | string | yes | Email for the primary contact. Client contacts must be included on mutating requests. |

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
| `settings` | object | Client-level settings object. |
| `updated_at` | number | Unix timestamp when the client was last updated. |

## Native endpoint

Through the native Invoice Ninja API, this operation is `POST /clients` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

