# Ship&Co: Register Shipping Address



```
POST https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-shipping-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-shipping-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "country": "string",
  "zip": "string",
  "address1": "string",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-shipping-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "country": "string",
    "zip": "string",
    "address1": "string",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | Recipient company. Required unless full name is provided. |
| `email` | string | no | Email address. |
| `full_name` | string | no | Recipient full name. Required unless company is provided. |
| `province` | string | no | Province or state code/name as required by destination country. |
| `country` | string | yes | ISO country code. |
| `zip` | string | yes | Postal code. |
| `address1` | string | yes | Primary street address. |
| `phone` | string | yes | Phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `created_at` | date |  |
| `id` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Ship&Co API, this operation is `POST /addresses` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-shipping-address.md) for the provider-specific parameters and requirements.

