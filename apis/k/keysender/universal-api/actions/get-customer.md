# Keysender: Get Customer

Retrieves a customer from Keysender.

```
GET https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-customer?${params}`, {
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
| `id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "language": "string",
      "lastName": "Chen",
      "listType": "string",
      "marketingFlag": true,
      "notes": "string",
      "organizationId": 1,
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Customer email. |
| `firstName` | string | Customer first name. |
| `id` | number | Customer identifier. |
| `language` | string | Customer language code. |
| `lastName` | string | Customer last name. |
| `listType` | string | Customer list type. |
| `marketingFlag` | boolean | Marketing opt-in flag. |
| `notes` | string | Customer notes. |
| `organizationId` | number | Organization identifier. |
| `phone` | string | Customer phone number. |

## Native endpoint

Through the native Keysender API, this operation is `GET /customer` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

