# AdvantShop: Get Bonus Card

Retrieves a bonus card from AdvantShop.

```
GET https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-bonus-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-bonus-card?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-bonus-card?${params}`, {
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
| `id` | string | yes | Bonus card number from AdvantShop. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cardId": 1,
      "cardNumber": "string",
      "customerId": "string",
      "gradeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `cardId` | number |  |
| `cardNumber` | string |  |
| `customerId` | string |  |
| `gradeName` | string |  |

## Native endpoint

Through the native AdvantShop API, this operation is `GET /bonus-cards/{id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bonus-card.md) for the provider-specific parameters and requirements.

