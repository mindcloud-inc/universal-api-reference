# Everbill: Create Customer

Creates a new customer in Everbill.

```
POST https://connect.mindcloud.co/v1/universal/everbill/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everbill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/everbill/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Customer": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everbill/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Customer": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Customer` | object | yes | Customer object for the request body. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Contact` | object | no | Contact object for the request body. |
| `Address` | object | no | Address object for the request body. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Everbill API returns.

## Native endpoint

Through the native Everbill API, this operation is `POST /customers/add` (base URL `https://api.everbill.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

