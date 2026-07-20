# MoneyBird: Get Product

Retrieves a product from MoneyBird.

```
GET https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoneyBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/get-product?connectionId=$CONNECTION_ID&administrationId=string&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "administrationId": "string",
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/get-product?${params}`, {
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
| `administrationId` | string | yes | Moneybird administration ID. |
| `productId` | string | yes | Moneybird product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrationId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "frequency": 1,
      "id": "string",
      "identifier": "string",
      "price": "string",
      "taxRateId": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `description` | string |  |
| `frequency` | number |  |
| `id` | string |  |
| `identifier` | string |  |
| `price` | string |  |
| `taxRateId` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native MoneyBird API, this operation is `GET /:administrationId/products/:productId.json` (base URL `https://moneybird.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

