# Autype: List Temporary Images

Retrieves temporary images from Autype.

```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-temporary-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-temporary-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-temporary-images?${params}`, {
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
      "images": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "expiresAt": "2026-05-07T12:00:00.000Z",
          "filename": "Ava Chen",
          "id": "string",
          "mimeType": "string",
          "refPath": "string",
          "sizeBytes": 1
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `images[].createdAt` | date |  |
| `images[].expiresAt` | date |  |
| `images[].filename` | string |  |
| `images[].id` | string |  |
| `images[].mimeType` | string |  |
| `images[].refPath` | string |  |
| `images[].sizeBytes` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Autype API, this operation is `GET /images` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-temporary-images.md) for the provider-specific parameters and requirements.

