# Spoonacular: Get Comparable Products

Retrieves comparable grocery products from Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/get-comparable-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/get-comparable-products?connectionId=$CONNECTION_ID&upc=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "upc": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/get-comparable-products?${params}`, {
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
| `upc` | string | yes | Required by the Spoonacular endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native Spoonacular API, this operation is `GET /food/products/upc/{upc}/comparable` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comparable-products.md) for the provider-specific parameters and requirements.

