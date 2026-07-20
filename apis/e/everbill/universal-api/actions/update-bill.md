# Everbill: Update Bill

Updates an existing bill in Everbill.

```
PUT https://connect.mindcloud.co/v1/universal/everbill/latest/actions/update-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everbill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/everbill/latest/actions/update-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "Bill": {},
  "Customer": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everbill/latest/actions/update-bill', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "Bill": {},
    "Customer": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Everbill record ID. |
| `Bill` | object | yes | Bill object for the request body. |
| `Customer` | object | yes | Customer object for the request body. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Address` | object | no | Address object for the request body. |
| `Article[]` | array<object> | no | Article array for the request body. |
| `Discount[]` | array<object> | no | Discount array for the request body. |
| `Transaction[]` | array<object> | no | Transaction array for the request body. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Everbill API returns.

## Native endpoint

Through the native Everbill API, this operation is `PUT /bills/update/:id` (base URL `https://api.everbill.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bill.md) for the provider-specific parameters and requirements.

