# Sellty: Delete Product



```
DELETE https://connect.mindcloud.co/v1/universal/sellty/latest/actions/delete-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sellty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sellty/latest/actions/delete-product?connectionId=$CONNECTION_ID&vendorCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vendorCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sellty/latest/actions/delete-product?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendorCode` | string | yes | Product SKU/vendor code to delete. |

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
| `status` | boolean | Whether the product was deleted. |

## Native endpoint

Through the native Sellty API, this operation is `POST /seller/api/v-1-0/delete-product` (base URL `https://my.sellty.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-product.md) for the provider-specific parameters and requirements.

