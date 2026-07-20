# Invoice Ninja: Show Client



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/show-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/show-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/show-client?${params}`, {
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
| `clientId` | string | yes | The Invoice Ninja hashed client ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Optional related resources to include, comma separated. |

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

Through the native Invoice Ninja API, this operation is `GET /clients/:id` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-client.md) for the provider-specific parameters and requirements.

