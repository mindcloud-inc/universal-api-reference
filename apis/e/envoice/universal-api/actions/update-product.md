# Envoice: Update Product

Updates an existing product in Envoice.

```
PUT https://connect.mindcloud.co/v1/universal/envoice/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currencyId": 1,
  "id": 1,
  "items": "string",
  "name": "Ava Chen",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currencyId": 1,
    "id": 1,
    "items": "string",
    "name": "Ava Chen",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currencyId` | number | yes | Currency identifier. |
| `description` | string | no | Product description. |
| `id` | number | yes | Product identifier. |
| `items` | string | yes | JSON array of product item objects. |
| `name` | string | yes | Product name. |
| `paymentGateways` | string | no | JSON array of product payment gateway objects. |
| `status` | string | yes | Product availability status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorMessages": [
        "string"
      ],
      "IsFaulted": true,
      "Success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorMessages` | array<string> | Error messages returned by Envoice. |
| `IsFaulted` | boolean | Whether the request failed. |
| `Success` | boolean | Whether the product was updated successfully. |

## Native endpoint

Through the native Envoice API, this operation is `POST product/update` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

