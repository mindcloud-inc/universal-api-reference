# Katana: Update Supplier

Updates an existing supplier in Katana.

```
PUT https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-supplier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Supplier id |
| `name` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `currency` | string | no | The supplier’s currency (ISO 4217). |
| `comment` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdAt": "string",
      "currency": "string",
      "deletedAt": "string",
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
| `comment` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `deletedAt` | string |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `PATCH /suppliers/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-supplier.md) for the provider-specific parameters and requirements.

