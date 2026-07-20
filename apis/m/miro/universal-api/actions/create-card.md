# Miro: Create Card

Creates a new card in Miro.

```
POST https://connect.mindcloud.co/v1/universal/miro/latest/actions/create-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Miro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/miro/latest/actions/create-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/miro/latest/actions/create-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | no | Target board ID. |
| `data.title` | string | yes | Title text for the new card |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "id": "string",
        "type": "string"
      },
      "data": {
        "assigneeId": "string",
        "description": "string",
        "dueDate": "2026-05-07T12:00:00.000Z",
        "title": "string"
      },
      "geometry": {
        "height": 1,
        "rotation": 1,
        "width": 1
      },
      "id": "string",
      "links": {
        "related": "https://example.com",
        "self": "https://example.com"
      },
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": {
        "id": "string",
        "type": "string"
      },
      "parent": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        }
      },
      "position": {
        "origin": "string",
        "relativeTo": "string",
        "slotId": "string",
        "x": 1,
        "y": 1
      },
      "style": {
        "cardTheme": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy.id` | string |  |
| `createdBy.type` | string |  |
| `data.assigneeId` | string |  |
| `data.description` | string |  |
| `data.dueDate` | date |  |
| `data.title` | string |  |
| `geometry.height` | number |  |
| `geometry.rotation` | number |  |
| `geometry.width` | number |  |
| `id` | string |  |
| `links.related` | string |  |
| `links.self` | string |  |
| `modifiedAt` | date |  |
| `modifiedBy.id` | string |  |
| `modifiedBy.type` | string |  |
| `parent.id` | string |  |
| `parent.links.self` | string |  |
| `position.origin` | string |  |
| `position.relativeTo` | string |  |
| `position.slotId` | string |  |
| `position.x` | number |  |
| `position.y` | number |  |
| `style.cardTheme` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Miro API, this operation is `POST /boards/:board_id/cards` (base URL `https://api.miro.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card.md) for the provider-specific parameters and requirements.

