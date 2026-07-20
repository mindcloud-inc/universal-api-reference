# Coast: Update Subscription Card By ID



```
PUT https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatesubscriptioncardbyid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatesubscriptioncardbyid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatesubscriptioncardbyid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | string | yes | Coast card ID of the card to update. |
| `status` | list | no | Updated status for the card. One of: `0`, `1`, `2`, `3`. |
| `name` | string | no | Updated name for the card. |
| `primaryPersonId` | string | no | Coast person ID whose name appears on purchases for this card. |
| `otherPersonIds[]` | array<string> | no | Other Coast people allowed to use this card in addition to the primary person. |
| `sharedByPersonId` | string | no | Coast person ID of the person sharing this card. |
| `spendLimit` | object | no | Updated spending limits for the card. |
| `requestReceipts` | boolean | no | Whether this card should require receipts. |
| `requestMemos` | boolean | no | Whether this card should require memos. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Coast API returns.

## Native endpoint

Through the native Coast API, this operation is `PATCH /v2/cards/:cardId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/updatesubscriptioncardbyid.md) for the provider-specific parameters and requirements.

