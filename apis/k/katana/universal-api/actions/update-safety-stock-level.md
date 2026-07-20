# Katana: Update Safety Stock Level

Updates an inventory safety stock level in Katana.

```
PUT https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-safety-stock-level
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-safety-stock-level" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "locationId": 1,
  "variantId": 1,
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-safety-stock-level', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "locationId": 1,
    "variantId": 1,
    "value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationId` | number | yes |  |
| `variantId` | number | yes |  |
| `value` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "locationId": 1,
      "updatedAt": "string",
      "value": 1,
      "variantId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `locationId` | number |  |
| `updatedAt` | string |  |
| `value` | number |  |
| `variantId` | number |  |

## Native endpoint

Through the native Katana API, this operation is `POST /inventory_safety_stock_levels` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-safety-stock-level.md) for the provider-specific parameters and requirements.

