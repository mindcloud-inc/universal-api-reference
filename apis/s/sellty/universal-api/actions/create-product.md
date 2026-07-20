# Sellty: Create Product



```
POST https://connect.mindcloud.co/v1/universal/sellty/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sellty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sellty/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sellty/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Product name. |
| `categoryId` | string | no | Product category ID. |
| `vendorCode` | string | no | Product SKU/vendor code. |
| `price` | number | no | Product price. |
| `amount` | number | no | Available product quantity. |
| `amountWait` | number | no | Expected product quantity. |
| `description` | string | no | Product description. |
| `status` | boolean | no | Product active status. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `volume` | string | no | Product volume. |
| `weight` | string | no | Product weight. |
| `length` | string | no | Product length. |
| `width` | string | no | Product width. |
| `height` | string | no | Product height. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | boolean | Whether the product was created. |

## Native endpoint

Through the native Sellty API, this operation is `POST /seller/api/v-1-0/add-product` (base URL `https://my.sellty.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

