# GorillaDesk: Create Customer

Creates a new customer in GorillaDesk.

```
POST https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GorillaDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "location": {},
  "location.addressLine1": "string",
  "location.city": "string",
  "location.state": "string",
  "location.zip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "location": {},
    "location.addressLine1": "string",
    "location.city": "string",
    "location.state": "string",
    "location.zip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountNumber` | string | no |  |
| `company` | string | no |  |
| `email` | string | no |  |
| `firstName` | string | yes |  |
| `lastName` | string | no |  |
| `location` | object | yes | Customer location object. |
| `location.addressLine1` | string | yes |  |
| `location.city` | string | yes |  |
| `location.state` | string | yes |  |
| `location.zip` | string | yes |  |
| `phones[]` | array<object> | no |  |
| `phones[].phone` | string | no |  |
| `phones[].type` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native GorillaDesk API, this operation is `POST /customers` (base URL `https://api.gorilladesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

