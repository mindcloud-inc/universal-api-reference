# Gorgias: Retrieve Customer

Retrieves a customer from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-customer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-customer?${params}`, {
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
| `id` | string | yes | Customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "channels": [
        {}
      ],
      "created_datetime": "string",
      "custom_fields": {},
      "data": {},
      "ecommerce_data": {},
      "email": "ava@example.com",
      "external_data": {},
      "firstname": "Ava",
      "id": 1,
      "integrations": [
        {}
      ],
      "language": "string",
      "lastname": "Chen",
      "meta": {},
      "name": "Ava Chen",
      "note": {},
      "timezone": "string",
      "updated_datetime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `channels` | array<object> |  |
| `created_datetime` | string |  |
| `custom_fields` | object |  |
| `data` | object |  |
| `ecommerce_data` | object |  |
| `email` | string |  |
| `external_data` | object |  |
| `firstname` | string |  |
| `id` | number |  |
| `integrations` | array<object> |  |
| `language` | string |  |
| `lastname` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `note` | object |  |
| `timezone` | string |  |
| `updated_datetime` | string |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /customers/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-customer.md) for the provider-specific parameters and requirements.

