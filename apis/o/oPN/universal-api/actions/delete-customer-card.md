# OPN: Delete Customer Card

Deletes an existing customer card from OPN.

```
DELETE https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-customer-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-customer-card?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-customer-card?${params}`, {
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
      "brand": "string",
      "created_at": "string",
      "deleted": true,
      "expiration_month": 1,
      "expiration_year": 1,
      "id": "string",
      "last_digits": "string",
      "livemode": true,
      "location": "string",
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string |  |
| `created_at` | string |  |
| `deleted` | boolean |  |
| `expiration_month` | number |  |
| `expiration_year` | number |  |
| `id` | string |  |
| `last_digits` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `name` | string |  |
| `object` | string |  |

## Native endpoint

Through the native OPN API, this operation is `DELETE /customers/:id/cards/:cardId` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer-card.md) for the provider-specific parameters and requirements.

