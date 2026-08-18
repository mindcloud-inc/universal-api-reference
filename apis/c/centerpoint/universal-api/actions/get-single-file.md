# Centerpoint: Get Single File



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-file?${params}`, {
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
| `fileId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "string",
        "deletedAt": {},
        "height": 1,
        "latitude": 1,
        "longitude": 1,
        "mimeType": "string",
        "thumbnailUrl": {},
        "title": {},
        "updatedAt": "string",
        "url": "https://example.com",
        "variety": "string",
        "width": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.height` | number |  |
| `attributes.latitude` | number |  |
| `attributes.longitude` | number |  |
| `attributes.mimeType` | string |  |
| `attributes.thumbnailUrl` | object |  |
| `attributes.title` | object |  |
| `attributes.updatedAt` | string |  |
| `attributes.url` | string |  |
| `attributes.variety` | string |  |
| `attributes.width` | number |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET files/:fileId` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-file.md) for the provider-specific parameters and requirements.

