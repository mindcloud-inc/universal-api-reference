# OPN: Get Customer Card

Retrieves details for a customer card from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-customer-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-customer-card?connectionId=$CONNECTION_ID&cardId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-customer-card?${params}`, {
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
| `cardId` | string | yes | The card ID to retrieve. |
| `id` | string | yes | The customer ID that owns the card. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bank": "string",
      "brand": "string",
      "city": "string",
      "country": "string",
      "created_at": "string",
      "deleted": true,
      "expiration_month": 1,
      "expiration_year": 1,
      "financing": "string",
      "fingerprint": "string",
      "first_digits": "string",
      "id": "string",
      "last_digits": "string",
      "livemode": true,
      "location": "string",
      "name": "Ava Chen",
      "object": "string",
      "phone_number": "string",
      "postal_code": "string",
      "security_code_check": true,
      "state": "string",
      "street1": "string",
      "street2": "string",
      "tokenization_method": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bank` | string |  |
| `brand` | string |  |
| `city` | string |  |
| `country` | string |  |
| `created_at` | string |  |
| `deleted` | boolean |  |
| `expiration_month` | number |  |
| `expiration_year` | number |  |
| `financing` | string |  |
| `fingerprint` | string |  |
| `first_digits` | string |  |
| `id` | string |  |
| `last_digits` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `name` | string |  |
| `object` | string |  |
| `phone_number` | string |  |
| `postal_code` | string |  |
| `security_code_check` | boolean |  |
| `state` | string |  |
| `street1` | string |  |
| `street2` | string |  |
| `tokenization_method` | string |  |

## Native endpoint

Through the native OPN API, this operation is `GET /customers/:id/cards/:cardId` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-card.md) for the provider-specific parameters and requirements.

