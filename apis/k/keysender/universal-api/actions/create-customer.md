# Keysender: Create Customer

Creates a customer in Keysender.

```
POST https://connect.mindcloud.co/v1/universal/keysender/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keysender/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native Keysender API, this operation is `POST /customer` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

