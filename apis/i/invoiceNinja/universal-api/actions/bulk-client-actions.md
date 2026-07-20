# Invoice Ninja: Bulk Client Actions



```
PUT https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-client-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-client-actions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "ids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-client-actions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "ids[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Bulk action to perform, such as archive, restore, delete, template, assign_group, or bulk_update. |
| `ids[]` | array<string> | yes | Array of client IDs to include in the bulk action. |
| `column` | string | no | Required for bulk_update. Invoice Ninja supports columns including public_notes, industry_id, size_id, country_id, and custom_value fields. |
| `newValue` | string | no | Required for bulk_update. New value to set on the selected column. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Optional related records to include in the response, such as contacts, documents, activities, ledger, or system_logs. |

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

Through the native Invoice Ninja API, this operation is `POST /clients/bulk` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-client-actions.md) for the provider-specific parameters and requirements.

