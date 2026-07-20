# Vistaly: Update Card

Updates an existing card in Vistaly.

```
PUT https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/update-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/update-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/update-card', {
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
| `cardId` | string | yes | The unique identifier for the card. |
| `cardTitle` | string | no | The updated title of the card. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardType` | list | no | The updated card type. One of: `assumption`, `experiment`, `kpi`, `objective`, `opportunity`, `outcome`, `problem`, `product`, `solution`. |
| `cardDetails` | string | no | The updated detailed description of the card. |
| `cardStatus` | list | no | The updated status of the card. One of: `addressed`, `at risk`, `developing`, `done`, `failed`, `idea`, `identified`, `later`, `next`, `not now`, `now`, `on track`, `passed`, `pending`, `progressing`, `running`, `uncommitted`. |
| `resources[]` | array<object> | no | Updated resource links for the card. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vistaly API returns.

## Native endpoint

Through the native Vistaly API, this operation is `PUT /beta/cards/{cardId}` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-card.md) for the provider-specific parameters and requirements.

