# Particle: Import Devices into Product



```
POST https://connect.mindcloud.co/v1/universal/particle/latest/actions/import-devices-into-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/particle/latest/actions/import-devices-into-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "0123456789abcdef01234567",
  "productIdOrSlug": "mindcloud-product"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/import-devices-into-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "0123456789abcdef01234567",
    "productIdOrSlug": "mindcloud-product"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Default: `0123456789abcdef01234567`. |
| `productIdOrSlug` | string | yes | Default: `mindcloud-product`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connected": true,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connected` | boolean |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Particle API, this operation is `POST /v1/products/:productIdOrSlug/devices` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-devices-into-product.md) for the provider-specific parameters and requirements.

