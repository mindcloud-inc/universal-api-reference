# Vistaly: Create Card

Creates a new card in Vistaly.

```
POST https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/create-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/create-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardTitle": "string",
  "parentId": "string",
  "parentType": "backlog"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/create-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardTitle": "string",
    "parentId": "string",
    "parentType": "backlog"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardTitle` | string | yes | The title of the card. |
| `parentId` | string | yes | The ID of the parent to associate with this card. |
| `parentType` | list | yes | The type of the parent. One of: `backlog`, `card`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardDetails` | string | no | The detailed description of the card. |
| `cardStatus` | list | no | The initial status of the card. One of: `addressed`, `at risk`, `developing`, `done`, `failed`, `idea`, `identified`, `later`, `next`, `not now`, `now`, `on track`, `passed`, `pending`, `progressing`, `running`, `uncommitted`. |
| `cardType` | list | no | The type of card to create. One of: `assumption`, `experiment`, `kpi`, `objective`, `opportunity`, `outcome`, `problem`, `product`, `solution`. |
| `resources[]` | array<object> | no | Optional resource links associated with the card. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardId": "string",
      "cardUrl": "https://example.com",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardId` | string |  |
| `cardUrl` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Vistaly API, this operation is `POST /beta/cards` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card.md) for the provider-specific parameters and requirements.

