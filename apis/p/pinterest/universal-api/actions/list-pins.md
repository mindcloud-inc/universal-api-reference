# Pinterest: List Pins

Retrieves the current user's pins from Pinterest.

```
GET https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-pins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinterest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-pins?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-pins?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "altText": {},
      "boardId": "string",
      "boardOwner": {
        "username": "Ava Chen"
      },
      "boardSectionId": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creativeType": "string",
      "description": "string",
      "dominantColor": "string",
      "hasBeenPromoted": true,
      "id": "string",
      "isOwner": true,
      "isStandard": true,
      "link": "https://example.com",
      "media": {
        "images": {
          "1200x": {
            "height": 1,
            "url": "https://example.com",
            "width": 1
          },
          "150x150": {
            "height": 1,
            "url": "https://example.com",
            "width": 1
          },
          "400x300": {
            "height": 1,
            "url": "https://example.com",
            "width": 1
          },
          "600x": {
            "height": 1,
            "url": "https://example.com",
            "width": 1
          }
        },
        "mediaType": "string"
      },
      "note": "string",
      "parentPinId": "string",
      "pinMetrics": {},
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altText` | object |  |
| `boardId` | string |  |
| `boardOwner.username` | string |  |
| `boardSectionId` | object |  |
| `createdAt` | date |  |
| `creativeType` | string |  |
| `description` | string |  |
| `dominantColor` | string |  |
| `hasBeenPromoted` | boolean |  |
| `id` | string |  |
| `isOwner` | boolean |  |
| `isStandard` | boolean |  |
| `link` | string |  |
| `media.images.1200x.height` | number |  |
| `media.images.1200x.url` | string |  |
| `media.images.1200x.width` | number |  |
| `media.images.150x150.height` | number |  |
| `media.images.150x150.url` | string |  |
| `media.images.150x150.width` | number |  |
| `media.images.400x300.height` | number |  |
| `media.images.400x300.url` | string |  |
| `media.images.400x300.width` | number |  |
| `media.images.600x.height` | number |  |
| `media.images.600x.url` | string |  |
| `media.images.600x.width` | number |  |
| `media.mediaType` | string |  |
| `note` | string |  |
| `parentPinId` | string |  |
| `pinMetrics` | object |  |
| `title` | string |  |

## Native endpoint

Through the native Pinterest API, this operation is `GET pins` (base URL `https://api.pinterest.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pins.md) for the provider-specific parameters and requirements.

