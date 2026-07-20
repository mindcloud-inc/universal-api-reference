# Coast: Order Subscription Virtual Card



```
POST https://connect.mindcloud.co/v1/universal/coast/latest/actions/ordersubscriptionvirtualcard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coast/latest/actions/ordersubscriptionvirtualcard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "creatorPersonId": "string",
  "primaryPersonId": "string",
  "otherPersonIds[]": [
    "string"
  ],
  "spendLimit": {},
  "requestReceipts": true,
  "requestMemos": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coast/latest/actions/ordersubscriptionvirtualcard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "creatorPersonId": "string",
    "primaryPersonId": "string",
    "otherPersonIds[]": ["string"],
    "spendLimit": {},
    "requestReceipts": true,
    "requestMemos": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the card. |
| `creatorPersonId` | string | yes | Coast person ID of the person creating this card. |
| `primaryPersonId` | string | yes | Coast person ID whose name appears on purchases for this card. |
| `otherPersonIds[]` | array<string> | yes | Other Coast people allowed to use this card in addition to the primary person. |
| `spendLimit` | object | yes | Spending limits for this card. |
| `requestReceipts` | boolean | yes | Whether this card should require receipts. |
| `requestMemos` | boolean | yes | Whether this card should require memos. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Coast API returns.

## Native endpoint

Through the native Coast API, this operation is `POST /v2/cards/virtual` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ordersubscriptionvirtualcard.md) for the provider-specific parameters and requirements.

