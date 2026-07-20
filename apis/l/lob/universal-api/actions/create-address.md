# Lob: Create Address



```
POST https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "addressLine1": "string",
  "addressCity": "string",
  "addressState": "string",
  "addressZip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/create-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "addressLine1": "string",
    "addressCity": "string",
    "addressState": "string",
    "addressZip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The recipient name for the address. |
| `addressLine1` | string | yes | The primary street address line. |
| `addressLine2` | string | no | The secondary street address line. |
| `addressCity` | string | yes | The city for the address. |
| `addressState` | string | yes | The state or region for the address. |
| `addressZip` | string | yes | The ZIP or postal code for the address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_city": "string",
      "address_country": "string",
      "address_line1": "string",
      "address_line2": "string",
      "address_state": "string",
      "address_zip": "string",
      "company": "string",
      "date_created": "string",
      "date_modified": "string",
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "phone": "string",
      "recipient_moved": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_city` | string |  |
| `address_country` | string |  |
| `address_line1` | string |  |
| `address_line2` | string |  |
| `address_state` | string |  |
| `address_zip` | string |  |
| `company` | string |  |
| `date_created` | string |  |
| `date_modified` | string |  |
| `description` | string |  |
| `email` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `object` | string |  |
| `phone` | string |  |
| `recipient_moved` | boolean |  |

## Native endpoint

Through the native Lob API, this operation is `POST /addresses` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-address.md) for the provider-specific parameters and requirements.

