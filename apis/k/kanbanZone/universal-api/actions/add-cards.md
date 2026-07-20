# Kanban Zone: Add Cards

Creates cards in Kanban Zone.

```
POST https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/add-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/add-cards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "board": "string",
  "cards[].title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/add-cards', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "board": "string",
    "cards[].title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `board` | string | yes | Board public ID for the cards to add |
| `addToTop` | boolean | no | Whether to add cards to the top of the target column |
| `cards[].title` | string | yes | Title for each card in the cards array |
| `cards[].columnId` | string | no | Column ID for each card |
| `cards[].description` | string | no | Description for each card |
| `cards[].templateId` | string | no | Card template public ID for each card |
| `cards[].blocked` | boolean | no | Blocked state for each card |
| `cards[].blockedBy` | string | no | Email of the member blocking the card |
| `cards[].blockedReason` | string | no | Blocked reason for each card |
| `cards[].dueAt` | string | no | Due date for each card |
| `cards[].owner` | string | no | Owner email for each card |
| `cards[].label` | string | no | Label name for each card |
| `cards[].watchers` | list<string> | no | Watcher email list for each card |
| `cards[].customFields[].label` | string | no | Custom field label for each card |
| `cards[].customFields[].value` | string | no | Custom field value for each card |
| `cards[].links.add[].card` | number | no | Card number to link to |
| `cards[].links.add[].type` | string | no | Relationship type for links to add |
| `cards[].links.add[].url` | string | no | External URL to link to |
| `cards[].links.add[].title` | string | no | Title for the external link |
| `cards[].links.remove[].card` | number | no | Card number of the link to remove |
| `cards[].links.remove[].url` | string | no | External URL of the link to remove |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cards": [
        {}
      ],
      "cardsAdded": 1,
      "errors": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cards` | array<object> |  |
| `cardsAdded` | number |  |
| `errors` | object |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `POST /cards` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-cards.md) for the provider-specific parameters and requirements.

