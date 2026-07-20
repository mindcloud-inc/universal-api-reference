# Kanban Zone: Move Card

Moves a card in Kanban Zone.

```
PUT https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/move-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/move-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "columnId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/move-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "columnId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Card number to move |
| `columnId` | string | yes | Destination column ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CardItem": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CardItem` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `POST /cards/:id/move` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-card.md) for the provider-specific parameters and requirements.

