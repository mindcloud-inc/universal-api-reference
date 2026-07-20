# Ordoro: Get Supplier Shipping Methods

Retrieves supplier shipping methods from Ordoro.

```
GET https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-supplier-shipping-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ordoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-supplier-shipping-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-supplier-shipping-methods?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Ordoro API, this operation is `GET /supplier/{supplier_id}/shipping_methods/` (base URL `https://api.ordoro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier-shipping-methods.md) for the provider-specific parameters and requirements.

