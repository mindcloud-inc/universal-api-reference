# KEYZY: Update Register Products

Registers a KEYZY product to a licensee.

```
PUT https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-register-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-register-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "name": "Ava Chen",
  "serial": "string",
  "skuNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-register-products', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "serial": "string",
    "skuNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email of the user. |
| `name` | string | yes | Name of the user. |
| `serial` | string | yes | A license serial number. |
| `skuNumber` | string | yes | SKU number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Register-products update confirmation message. |

## Native endpoint

Through the native KEYZY API, this operation is `PUT /register-products/:serial` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-register-products.md) for the provider-specific parameters and requirements.

