# Zakeke: Import Provider Products



```
POST https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/import-provider-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zakeke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/import-provider-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/import-provider-products', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `products[]` | array<object> | no | Provider product list to import. |
| `productTypes[]` | array<object> | no | Provider product types and print constraints. |
| `version` | string | no | Optional payload version. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `canvasBorders[]` | array<object> | no | Optional provider canvas borders. |
| `multiCanvasSettings[]` | array<object> | no | Optional provider multi-canvas settings. |
| `product3DSettings[]` | array<object> | no | Optional provider 3D settings. |
| `resizableSettings[]` | array<object> | no | Optional provider resizable settings. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zakeke API returns.

## Native endpoint

Through the native Zakeke API, this operation is `POST /v2/providerproducts/import` (base URL `https://api.zakeke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-provider-products.md) for the provider-specific parameters and requirements.

