# Coast: Order Project Virtual Card



```
POST https://connect.mindcloud.co/v1/universal/coast/latest/actions/orderprojectvirtualcard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coast/latest/actions/orderprojectvirtualcard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "projectBudgetId": "string",
  "primaryPersonId": "string",
  "spendLimit": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coast/latest/actions/orderprojectvirtualcard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "projectBudgetId": "string",
    "primaryPersonId": "string",
    "spendLimit": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the card. |
| `projectBudgetId` | string | yes | Coast project budget ID permanently assigned to this card. |
| `primaryPersonId` | string | yes | Coast person ID whose name appears on purchases for this card. |
| `spendLimit` | object | yes | Spending limits for this card. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Coast API returns.

## Native endpoint

Through the native Coast API, this operation is `POST /v2/cards/virtual` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/orderprojectvirtualcard.md) for the provider-specific parameters and requirements.

