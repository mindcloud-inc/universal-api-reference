# Ship&Co: Register Warehouse



```
POST https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-warehouse
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-warehouse" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/register-warehouse', {
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
| `company` | string | no | Warehouse company name. |
| `email` | string | no | Warehouse email address. |
| `full_name` | string | no | Warehouse contact full name. Required unless another supported name field is present. |
| `province_kanji` | string | no | Required for warehouses located in Japan. |
| `country` | string | yes | ISO country code. |
| `zip` | string | yes | Postal code. |
| `address1` | string | yes | Primary warehouse address. |
| `phone` | string | yes | Warehouse phone number. |

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

Through the native Ship&Co API, this operation is `POST /warehouses` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-warehouse.md) for the provider-specific parameters and requirements.

