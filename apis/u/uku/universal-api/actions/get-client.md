# Uku: Get Client

Retrieves a client from Uku.

```
GET https://connect.mindcloud.co/v1/universal/uku/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uku `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uku/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uku/latest/actions/get-client?${params}`, {
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
| `clientId` | string | yes | Uku client ID |

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

Through the native Uku API, this operation is `GET /clients/:clientId` (base URL `https://app.getuku.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

