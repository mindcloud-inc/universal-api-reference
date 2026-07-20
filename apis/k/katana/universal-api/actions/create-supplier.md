# Katana: Create Supplier

Creates a new supplier in Katana.

```
POST https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-supplier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `currency` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `comment` | string | no |  |
| `addresses[]` | array<object> | no |  |
| `addresses[].line1` | string | no |  |
| `addresses[].line2` | string | no |  |
| `addresses[].city` | string | no |  |
| `addresses[].state` | string | no |  |
| `addresses[].zip` | string | no |  |
| `addresses[].country` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "city": "string",
          "country": "string",
          "createdAt": "string",
          "id": 1,
          "line1": "string",
          "line2": "string",
          "state": "string",
          "supplierId": 1,
          "updatedAt": "string",
          "zip": "string"
        }
      ],
      "comment": "string",
      "createdAt": "string",
      "currency": "string",
      "defaultAddressId": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `addresses[].city` | string |  |
| `addresses[].country` | string |  |
| `addresses[].createdAt` | string |  |
| `addresses[].id` | number |  |
| `addresses[].line1` | string |  |
| `addresses[].line2` | string |  |
| `addresses[].state` | string |  |
| `addresses[].supplierId` | number |  |
| `addresses[].updatedAt` | string |  |
| `addresses[].zip` | string |  |
| `comment` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `defaultAddressId` | number |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `POST /suppliers` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-supplier.md) for the provider-specific parameters and requirements.

