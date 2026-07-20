# Miro: Update Item Position

Updates an item's position or parent in Miro.

```
PUT https://connect.mindcloud.co/v1/universal/miro/latest/actions/update-item-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Miro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/miro/latest/actions/update-item-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/miro/latest/actions/update-item-position', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | no | Target board ID. |
| `itemId` | string | no | Target item ID. |

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
        "altText": "string",
        "assigneeId": "string",
        "content": "string",
        "contentType": "string",
        "description": "string",
        "documentUrl": "https://example.com",
        "dueDate": "2026-05-07T12:00:00.000Z",
        "fields": [
          {
            "fillColor": "string",
            "iconShape": "string",
            "iconUrl": "https://example.com",
            "textColor": "string",
            "tooltip": "string",
            "value": "string"
          }
        ],
        "format": "string",
        "html": "string",
        "imageUrl": "https://example.com",
        "mode": "string",
        "owned": true,
        "previewUrl": "https://example.com",
        "providerName": "Ava Chen",
        "providerUrl": "https://example.com",
        "shape": "string",
        "showContent": true,
        "status": "string",
        "title": "string",
        "type": "string",
        "url": "https://example.com"
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
| `data.altText` | string |  |
| `data.assigneeId` | string |  |
| `data.content` | string |  |
| `data.contentType` | string |  |
| `data.description` | string |  |
| `data.documentUrl` | string |  |
| `data.dueDate` | date |  |
| `data.fields[].fillColor` | string |  |
| `data.fields[].iconShape` | string |  |
| `data.fields[].iconUrl` | string |  |
| `data.fields[].textColor` | string |  |
| `data.fields[].tooltip` | string |  |
| `data.fields[].value` | string |  |
| `data.format` | string |  |
| `data.html` | string |  |
| `data.imageUrl` | string |  |
| `data.mode` | string |  |
| `data.owned` | boolean |  |
| `data.previewUrl` | string |  |
| `data.providerName` | string |  |
| `data.providerUrl` | string |  |
| `data.shape` | string |  |
| `data.showContent` | boolean |  |
| `data.status` | string |  |
| `data.title` | string |  |
| `data.type` | string |  |
| `data.url` | string |  |
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

Through the native Miro API, this operation is `PATCH /boards/:board_id/items/:item_id` (base URL `https://api.miro.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item-position.md) for the provider-specific parameters and requirements.

