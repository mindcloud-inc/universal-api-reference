# Kanban Zone: Update Card

Updates an existing card in Kanban Zone.

```
PUT https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/update-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/update-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/update-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The number of the card to update |
| `title` | string | yes | Card title |
| `board` | string | no | Board public ID for the mirror card to update |
| `columnId` | string | no | Column ID for the card |
| `description` | string | no | Card description |
| `templateId` | string | no | Card template public ID |
| `blocked` | boolean | no | Blocked state for the card |
| `blockedBy` | string | no | Email of the member blocking the card |
| `blockedReason` | string | no | Blocked reason for the card |
| `dueAt` | string | no | Due date for the card |
| `owner` | string | no | Owner email for the card |
| `label` | string | no | Label name for the card |
| `watchers` | list<string> | no | Watcher email list |
| `customFields[].label` | string | no | Custom field label |
| `customFields[].value` | string | no | Custom field value |
| `links.add[].card` | number | no | Card number to link to |
| `links.add[].type` | string | no | Relationship type for links to add |
| `links.add[].url` | string | no | External URL to link to |
| `links.add[].title` | string | no | Title for the external link |
| `links.remove[].card` | number | no | Card number of the link to remove |
| `links.remove[].url` | string | no | External URL of the link to remove |

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

Through the native Kanban Zone API, this operation is `PUT /cards/:id` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-card.md) for the provider-specific parameters and requirements.

