# Faire: Update inventory by SKUs



```
GET https://connect.mindcloud.co/v1/universal/Faire/latest/actions/update-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/Faire/latest/actions/update-inventory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/Faire/latest/actions/update-inventory?${params}`, {
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
| `inventories[].sku` | string | no |  |
| `inventories[].onHandquantity` | number | no |  |
| `inventories[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Faire API returns.

## Native endpoint

Through the native Faire API, this operation is `PATCH product-inventory/by-skus` (base URL `https://www.faire.com/external-api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inventory.md) for the provider-specific parameters and requirements.

