# BASIC: Get project images

Retrieves project icon and background images from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-project-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-project-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-project-images?${params}`, {
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
      "images": {
        "background": {
          "background_url": "https://example.com",
          "contentType": "string",
          "lastModified": "2026-05-07T12:00:00.000Z",
          "size": 1
        },
        "icon": {
          "contentType": "string",
          "icon_url": "https://example.com",
          "lastModified": "2026-05-07T12:00:00.000Z",
          "size": 1
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `images.background.background_url` | string |  |
| `images.background.contentType` | string |  |
| `images.background.lastModified` | date |  |
| `images.background.size` | number |  |
| `images.icon.contentType` | string |  |
| `images.icon.icon_url` | string |  |
| `images.icon.lastModified` | date |  |
| `images.icon.size` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /project/{id}/upload` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-images.md) for the provider-specific parameters and requirements.

