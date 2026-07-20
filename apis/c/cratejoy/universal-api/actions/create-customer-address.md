# Cratejoy: Create Customer Address

Creates a customer address in Cratejoy.

```
POST https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/create-customer-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/create-customer-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/create-customer-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | The Cratejoy customer ID. |
| `to` | string | no | The name on the address. |
| `street` | string | no | The street line for the address. |
| `city` | string | no | The city for the address. |
| `state` | string | no | The state or province for the address. |
| `zipCode` | string | no | The postal code for the address. |
| `country` | string | no | The two-letter country code for the address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "id": 1,
      "state": "string",
      "status": 1,
      "status_message": "string",
      "street": "string",
      "to": "string",
      "url": "https://example.com",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `id` | number |  |
| `state` | string |  |
| `status` | number |  |
| `status_message` | string |  |
| `street` | string |  |
| `to` | string |  |
| `url` | string |  |
| `zip_code` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `POST /v1/customers/:customerId/addresses/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-address.md) for the provider-specific parameters and requirements.

