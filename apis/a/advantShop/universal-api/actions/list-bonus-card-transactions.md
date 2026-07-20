# AdvantShop: List Bonus Card Transactions

Retrieves bonus card transactions from AdvantShop.

```
GET https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/list-bonus-card-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/list-bonus-card-transactions?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/list-bonus-card-transactions?${params}`, {
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
      "basis": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `basis` | string |  |
| `date` | date |  |
| `id` | number |  |
| `type` | string |  |

## Native endpoint

Through the native AdvantShop API, this operation is `GET /bonus-cards/{id}/transactions` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bonus-card-transactions.md) for the provider-specific parameters and requirements.

