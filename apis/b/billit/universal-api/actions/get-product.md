# Billit: Get Product

Retrieves a Billit product by ID.

```
GET https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-product?connectionId=$CONNECTION_ID&productID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-product?${params}`, {
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
| `productID` | number | yes | Billit ProductID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Description": "string",
      "ProductID": 1,
      "UnitPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string | Billit product description. |
| `ProductID` | number | Billit product identifier. |
| `UnitPrice` | number | Billit unit price when present. |

## Native endpoint

Through the native Billit API, this operation is `GET /v1/products/:productID` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

