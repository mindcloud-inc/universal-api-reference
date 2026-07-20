# Miro: List Items

Retrieves items from a Miro board.

```
GET https://connect.mindcloud.co/v1/universal/miro/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Miro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/miro/latest/actions/list-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/miro/latest/actions/list-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | no | Target board ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
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
          "type": "string"
        }
      ],
      "limit": 1,
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com",
        "self": "https://example.com"
      },
      "size": 1,
      "total": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `data` | array |  |
| `data[].createdAt` | date |  |
| `data[].createdBy.id` | string |  |
| `data[].createdBy.type` | string |  |
| `data[].data.altText` | string |  |
| `data[].data.assigneeId` | string |  |
| `data[].data.content` | string |  |
| `data[].data.contentType` | string |  |
| `data[].data.description` | string |  |
| `data[].data.documentUrl` | string |  |
| `data[].data.dueDate` | date |  |
| `data[].data.fields[].fillColor` | string |  |
| `data[].data.fields[].iconShape` | string |  |
| `data[].data.fields[].iconUrl` | string |  |
| `data[].data.fields[].textColor` | string |  |
| `data[].data.fields[].tooltip` | string |  |
| `data[].data.fields[].value` | string |  |
| `data[].data.format` | string |  |
| `data[].data.html` | string |  |
| `data[].data.imageUrl` | string |  |
| `data[].data.mode` | string |  |
| `data[].data.owned` | boolean |  |
| `data[].data.previewUrl` | string |  |
| `data[].data.providerName` | string |  |
| `data[].data.providerUrl` | string |  |
| `data[].data.shape` | string |  |
| `data[].data.showContent` | boolean |  |
| `data[].data.status` | string |  |
| `data[].data.title` | string |  |
| `data[].data.type` | string |  |
| `data[].data.url` | string |  |
| `data[].geometry.height` | number |  |
| `data[].geometry.rotation` | number |  |
| `data[].geometry.width` | number |  |
| `data[].id` | string |  |
| `data[].links.related` | string |  |
| `data[].links.self` | string |  |
| `data[].modifiedAt` | date |  |
| `data[].modifiedBy.id` | string |  |
| `data[].modifiedBy.type` | string |  |
| `data[].parent.id` | string |  |
| `data[].parent.links.self` | string |  |
| `data[].position.origin` | string |  |
| `data[].position.relativeTo` | string |  |
| `data[].position.slotId` | string |  |
| `data[].position.x` | number |  |
| `data[].position.y` | number |  |
| `data[].type` | string |  |
| `limit` | number |  |
| `links.first` | string |  |
| `links.last` | string |  |
| `links.next` | string |  |
| `links.prev` | string |  |
| `links.self` | string |  |
| `size` | number |  |
| `total` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Miro API, this operation is `GET /boards/:board_id/items` (base URL `https://api.miro.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

