# Understory: List Ticket Variants

Retrieves ticket variants for an experience in Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-ticket-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-ticket-variants?connectionId=$CONNECTION_ID&limit=25&offset=0&experienceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "experienceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-ticket-variants?${params}`, {
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
| `experienceId` | string | yes | The unique identifier of the experience. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "add_on_variants": [
            {
              "description": "string",
              "id": "string",
              "name": "Ava Chen",
              "price": {
                "currency": "string",
                "exponent": 1,
                "value": 1
              },
              "vat_amount": {
                "currency": "string",
                "exponent": 1,
                "value": 1
              }
            }
          ],
          "description": "string",
          "id": "string",
          "name": "Ava Chen",
          "price": {
            "currency": "string",
            "exponent": 1,
            "value": 1
          },
          "vat_amount": {
            "currency": "string",
            "exponent": 1,
            "value": 1
          }
        }
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].add_on_variants[].description` | string |  |
| `items[].add_on_variants[].id` | string |  |
| `items[].add_on_variants[].name` | string |  |
| `items[].add_on_variants[].price.currency` | string |  |
| `items[].add_on_variants[].price.exponent` | number |  |
| `items[].add_on_variants[].price.value` | number |  |
| `items[].add_on_variants[].vat_amount.currency` | string |  |
| `items[].add_on_variants[].vat_amount.exponent` | number |  |
| `items[].add_on_variants[].vat_amount.value` | number |  |
| `items[].description` | string |  |
| `items[].id` | string |  |
| `items[].name` | string |  |
| `items[].price.currency` | string |  |
| `items[].price.exponent` | number |  |
| `items[].price.value` | number |  |
| `items[].vat_amount.currency` | string |  |
| `items[].vat_amount.exponent` | number |  |
| `items[].vat_amount.value` | number |  |
| `next` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/experiences/{{experienceId}}/ticket-variants` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ticket-variants.md) for the provider-specific parameters and requirements.

