# Cryptolens: List Products

Retrieves products from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/list-products?${params}`, {
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
| `v` | string | no | Method version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "string",
      "dataObjects": [
        "string"
      ],
      "description": "string",
      "featureDefinitions": {},
      "id": 1,
      "isPublic": true,
      "keyAlgorithm": 1,
      "name": "Ava Chen",
      "password": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | string | Product creation date from the Cryptolens docs example. |
| `dataObjects` | array<string> | Product data objects from the Cryptolens docs example. |
| `description` | string | Product description from the Cryptolens docs example. |
| `featureDefinitions` | object | Feature definition map from the Cryptolens docs example. |
| `id` | number | Product ID from the Cryptolens docs example. |
| `isPublic` | boolean | Whether the product is public in the Cryptolens docs example. |
| `keyAlgorithm` | number | Key algorithm identifier from the Cryptolens docs example. |
| `name` | string | Product name from the Cryptolens docs example. |
| `password` | string | Product password field from the Cryptolens docs example. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/product/GetProducts` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

