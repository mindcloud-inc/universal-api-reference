# Uku: Create Client

Creates a new client in Uku.

```
POST https://connect.mindcloud.co/v1/universal/uku/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uku `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uku/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addressCountryCode": "string",
  "clientInitials": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uku/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addressCountryCode": "string",
    "clientInitials": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressCountryCode` | string | yes | ISO country code |
| `clientInitials` | string | yes | Client initials |
| `name` | string | yes | Client name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "address_country_code": "string",
      "billing_settings": {},
      "client_initials": "string",
      "contacts": [
        {}
      ],
      "created_at": "string",
      "default_person_id": 1,
      "fields": {},
      "groups": [
        {}
      ],
      "id": 1,
      "locale_code": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `address_country_code` | string |  |
| `billing_settings` | object |  |
| `client_initials` | string |  |
| `contacts` | array<object> |  |
| `created_at` | string |  |
| `default_person_id` | number |  |
| `fields` | object |  |
| `groups` | array<object> |  |
| `id` | number |  |
| `locale_code` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uku API, this operation is `POST /clients` (base URL `https://app.getuku.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

